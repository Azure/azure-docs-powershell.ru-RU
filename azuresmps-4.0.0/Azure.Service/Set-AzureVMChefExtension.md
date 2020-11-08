---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076045"
---
# <span data-ttu-id="2d510-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d510-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="2d510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d510-102">SYNOPSIS</span></span>
<span data-ttu-id="2d510-103">Добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2d510-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2d510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d510-104">SYNTAX</span></span>

### <span data-ttu-id="2d510-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d510-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2d510-106">Linux</span><span class="sxs-lookup"><span data-stu-id="2d510-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2d510-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d510-107">DESCRIPTION</span></span>
<span data-ttu-id="2d510-108">Командлет **Set-AzureVMChefExtension** добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2d510-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2d510-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d510-109">EXAMPLES</span></span>

### <span data-ttu-id="2d510-110">Пример 1: Добавление расширения Chef на виртуальную машину Windows</span><span class="sxs-lookup"><span data-stu-id="2d510-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="2d510-111">Эта команда добавляет расширение Chef на виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="2d510-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="2d510-112">После появлении виртуальной машины она загруза с помощью Chef и выполнит на ней Apache.</span><span class="sxs-lookup"><span data-stu-id="2d510-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="2d510-113">Пример 2: Добавление расширения Chef для виртуальной машины Windows с помощью начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="2d510-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="2d510-114">Эта команда добавляет расширение Chef на виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="2d510-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="2d510-115">После запуска виртуальная машина загруза ее с помощью Chef, и на ней запускается Apache.</span><span class="sxs-lookup"><span data-stu-id="2d510-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="2d510-116">После начальной загрузки виртуальная машина ссылается на *BootstrapOptions* , указанный в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2d510-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="2d510-117">Пример 3: Добавление расширения Chef на виртуальную машину Windows и установка Apache и GIT</span><span class="sxs-lookup"><span data-stu-id="2d510-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="2d510-118">Эта команда добавляет расширение Chef на виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="2d510-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="2d510-119">При запуске виртуальной машины она загруза с помощью Chef, и на ней установлен компонент Apache и GIT.</span><span class="sxs-lookup"><span data-stu-id="2d510-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="2d510-120">Если вы не предоставляете клиент. RB, вам нужно указать URL-адрес сервера Chef и имя клиента проверки.</span><span class="sxs-lookup"><span data-stu-id="2d510-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="2d510-121">Пример 4: Добавление расширения Chef на виртуальную машину Linux</span><span class="sxs-lookup"><span data-stu-id="2d510-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="2d510-122">Эта команда добавляет расширение Chef на виртуальную машину Linux.</span><span class="sxs-lookup"><span data-stu-id="2d510-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="2d510-123">После запуска виртуальная машина загруза ее с помощью Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="2d510-124">Если вы не предоставляете клиент. RB, вам нужно указать URL-адрес и организацию сервера Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="2d510-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d510-125">PARAMETERS</span></span>

### <span data-ttu-id="2d510-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="2d510-126">-BootstrapOptions</span></span>
<span data-ttu-id="2d510-127">Задает параметры начальной загрузки в формате JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="2d510-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="2d510-128">-BootstrapVersion</span></span>
<span data-ttu-id="2d510-129">Определяет версию клиента Chef, установленного вместе с расширением.</span><span class="sxs-lookup"><span data-stu-id="2d510-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="2d510-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="2d510-131">Определяет частоту (в минутах), с которой работает Chef-служба.</span><span class="sxs-lookup"><span data-stu-id="2d510-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="2d510-132">Если вы не хотите, чтобы Chef-служба была установлена на виртуальной машине Azure, установите для этого поля значение 0.</span><span class="sxs-lookup"><span data-stu-id="2d510-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="2d510-133">-ChefServerUrl</span></span>
<span data-ttu-id="2d510-134">Указывает URL-адрес сервера Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-134">Specifies the URL of the Chef server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="2d510-135">-ClientRb</span></span>
<span data-ttu-id="2d510-136">Указывает полный путь к Chef Client. RB.</span><span class="sxs-lookup"><span data-stu-id="2d510-136">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-137">-Демон</span><span class="sxs-lookup"><span data-stu-id="2d510-137">-Daemon</span></span>
<span data-ttu-id="2d510-138">Настраивает службу Chef-Client для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d510-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="2d510-139">Платформа узла должна быть Windows.</span><span class="sxs-lookup"><span data-stu-id="2d510-139">The node platform should be Windows.</span></span>
<span data-ttu-id="2d510-140">Разрешенные варианты: "нет", "служба" и "задача".</span><span class="sxs-lookup"><span data-stu-id="2d510-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="2d510-141">None — в настоящее время служба Chef-клиента не будет настроена как служба.</span><span class="sxs-lookup"><span data-stu-id="2d510-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="2d510-142">Служба — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="2d510-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="2d510-143">задача — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве задачи secheduled.</span><span class="sxs-lookup"><span data-stu-id="2d510-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2d510-144">-InformationAction</span></span>
<span data-ttu-id="2d510-145">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="2d510-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2d510-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2d510-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d510-147">Продолжал</span><span class="sxs-lookup"><span data-stu-id="2d510-147">Continue</span></span>
- <span data-ttu-id="2d510-148">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="2d510-148">Ignore</span></span>
- <span data-ttu-id="2d510-149">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="2d510-149">Inquire</span></span>
- <span data-ttu-id="2d510-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2d510-150">SilentlyContinue</span></span>
- <span data-ttu-id="2d510-151">Остановить</span><span class="sxs-lookup"><span data-stu-id="2d510-151">Stop</span></span>
- <span data-ttu-id="2d510-152">Рвать</span><span class="sxs-lookup"><span data-stu-id="2d510-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2d510-153">-InformationVariable</span></span>
<span data-ttu-id="2d510-154">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="2d510-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="2d510-155">-JsonAttribute</span></span>
<span data-ttu-id="2d510-156">Строка JSON, добавляемая в первый запуск Chef-Client.</span><span class="sxs-lookup"><span data-stu-id="2d510-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="2d510-157">Например,-JsonAttribute ' {"foo": "отрезок"} "</span><span class="sxs-lookup"><span data-stu-id="2d510-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="2d510-158">-Linux</span></span>
<span data-ttu-id="2d510-159">Указывает на то, что этот командлет создает виртуальную машину на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="2d510-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-160">-Название_организации</span><span class="sxs-lookup"><span data-stu-id="2d510-160">-OrganizationName</span></span>
<span data-ttu-id="2d510-161">Указывает название организации для расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-161">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-162">-Profile</span><span class="sxs-lookup"><span data-stu-id="2d510-162">-Profile</span></span>
<span data-ttu-id="2d510-163">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2d510-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d510-164">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d510-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="2d510-165">-RunList</span></span>
<span data-ttu-id="2d510-166">Указывает список выполнения для узла Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-166">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-167">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="2d510-167">-Secret</span></span>
<span data-ttu-id="2d510-168">Ключ шифрования, используемый для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="2d510-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="2d510-169">-SecretFile</span></span>
<span data-ttu-id="2d510-170">Путь к файлу, содержащему ключ шифрования, который используется для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="2d510-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="2d510-171">-ValidationClientName</span></span>
<span data-ttu-id="2d510-172">Указывает имя клиента проверки.</span><span class="sxs-lookup"><span data-stu-id="2d510-172">Specifies the name of the validation client.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="2d510-173">-ValidationPem</span></span>
<span data-ttu-id="2d510-174">Задает путь к файлу проверяющего элемента управления Chef. PEM.</span><span class="sxs-lookup"><span data-stu-id="2d510-174">Specifies the Chef validator .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-175">-Version</span><span class="sxs-lookup"><span data-stu-id="2d510-175">-Version</span></span>
<span data-ttu-id="2d510-176">Указывает номер версии расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="2d510-176">Specifies the version number of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-177">-VM</span><span class="sxs-lookup"><span data-stu-id="2d510-177">-VM</span></span>
<span data-ttu-id="2d510-178">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d510-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="2d510-179">-Windows</span></span>
<span data-ttu-id="2d510-180">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="2d510-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d510-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d510-181">CommonParameters</span></span>
<span data-ttu-id="2d510-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d510-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d510-183">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d510-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d510-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d510-184">INPUTS</span></span>

## <span data-ttu-id="2d510-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d510-185">OUTPUTS</span></span>

## <span data-ttu-id="2d510-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d510-186">NOTES</span></span>

## <span data-ttu-id="2d510-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d510-187">RELATED LINKS</span></span>

[<span data-ttu-id="2d510-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d510-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="2d510-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2d510-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


