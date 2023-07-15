import React from 'react';
import './styles.css';

const plans = [
  {
    id: 'basic',
    price: '3.99$',
    disk_space: '100GB',
    data_transfer: '1000GB/Month',
    site_pages: '10'
  },
  {
    id: 'Professional',
    price: '5.99$',
    disk_space: '500GB',
    data_transfer: '5000GB/Month',
    site_pages: '50'
  },
  {
    id: 'ultimate',
    price: '9.99$',
    disk_space: '2000GB',
    data_transfer: '20000GB/Month',
    site_pages: '500'
  },
];

const App = () => {
  const show_basic_items = plans.filter((hosting_basic) => hosting_basic.id === 'basic');
  const show_prof_items = plans.filter((hosting_professional) => hosting_professional.id === 'Professional');
  const show_ultimate_items = plans.filter((hosting_ultimate) => hosting_ultimate.id === 'ultimate');

  const rendering_basic = show_basic_items.map((basic) => (
    <table key={basic.id}>
      <tbody>
        <tr>
          <td>{basic.id}</td>
        </tr>
        <tr>
          <td>{basic.price}</td>
        </tr>
        <tr>
          <td>{basic.disk_space}</td>
        </tr>
        <tr>
          <td>{basic.data_transfer}</td>
        </tr>
        <tr>
          <td>{basic.site_pages}</td>
        </tr>
      </tbody>
    </table>
  ));

  const rendering_professional = show_prof_items.map((professional) => (
    <table key={professional.id}>
      <tbody>
        <tr>
          <td>{professional.id}</td>
        </tr>
        <tr>
          <td>{professional.price}</td>
        </tr>
        <tr>
          <td>{professional.disk_space}</td>
        </tr>
        <tr>
          <td>{professional.data_transfer}</td>
        </tr>
        <tr>
          <td>{professional.site_pages}</td>
        </tr>
      </tbody>
    </table>
  ));

  const rendering_ultimate = show_ultimate_items.map((ultimate) => (
    <table key={ultimate.id}>
      <tbody>
        <tr>
          <td>{ultimate.id}</td>
        </tr>
        <tr>
          <td>{ultimate.price}</td>
        </tr>
        <tr>
          <td>{ultimate.disk_space}</td>
        </tr>
        <tr>
          <td>{ultimate.data_transfer}</td>
        </tr>
        <tr>
          <td>{ultimate.site_pages}</td>
        </tr>
      </tbody>
    </table>
  ));

  return (
    <div className="App">
      {rendering_basic}
      {rendering_professional}
      {rendering_ultimate}
    </div>
  );
};

export default App;
