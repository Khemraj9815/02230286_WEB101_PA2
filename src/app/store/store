import {create} from 'zustand';

const useStore = create((set) => ({
  caughtPokemons: JSON.parse(localStorage.getItem('caughtPokemons')) || [],
  addCaughtPokemon: (pokemon) =>
    set((state) => {
      const updatedCaughtPokemons = [...state.caughtPokemons, pokemon];
      localStorage.setItem('caughtPokemons', JSON.stringify(updatedCaughtPokemons));
      return { caughtPokemons: updatedCaughtPokemons };
    }),
  clearCaughtPokemons: () =>
    set(() => {
      localStorage.removeItem('caughtPokemons');
      return { caughtPokemons: [] };
    }),
}));

export default useStore;
