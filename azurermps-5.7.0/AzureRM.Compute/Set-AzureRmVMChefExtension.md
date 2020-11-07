---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25ddfd3fcb7d087db493e87bdd9781b2bbb77040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732159"
---
# <span data-ttu-id="79401-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="79401-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="79401-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79401-102">SYNOPSIS</span></span>
<span data-ttu-id="79401-103">Добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="79401-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79401-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79401-104">SYNTAX</span></span>

### <span data-ttu-id="79401-105">Linux</span><span class="sxs-lookup"><span data-stu-id="79401-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79401-106">Windows</span><span class="sxs-lookup"><span data-stu-id="79401-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79401-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79401-107">DESCRIPTION</span></span>
<span data-ttu-id="79401-108">Командлет **Set-AzureVMChefExtension** добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="79401-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="79401-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79401-109">EXAMPLES</span></span>

### <span data-ttu-id="79401-110">Пример 1: Добавление расширения Chef на виртуальную машину Windows</span><span class="sxs-lookup"><span data-stu-id="79401-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="79401-111">Эта команда добавляет расширение Chef на виртуальную машину Windows с именем WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="79401-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="79401-112">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="79401-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="79401-113">Пример 2: Добавление расширения Chef на виртуальную машину Linux</span><span class="sxs-lookup"><span data-stu-id="79401-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="79401-114">Эта команда добавляет расширение Chef на виртуальную машину Linux с именем LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="79401-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="79401-115">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="79401-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="79401-116">Пример 3: Добавление расширения Chef для виртуальной машины Windows с помощью параметров начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="79401-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="79401-117">Эта команда добавляет расширение Chef на виртуальную машину Windows с именем WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="79401-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="79401-118">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="79401-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="79401-119">После начальной загрузки виртуальная машина ссылается на BootstrapOptions, указанный в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="79401-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="79401-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79401-120">PARAMETERS</span></span>

### <span data-ttu-id="79401-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="79401-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="79401-122">-BootstrapOptions</span></span>
<span data-ttu-id="79401-123">Задает параметры конфигурации в параметре client_rb.</span><span class="sxs-lookup"><span data-stu-id="79401-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="79401-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="79401-124">-BootstrapVersion</span></span>
<span data-ttu-id="79401-125">Задает версию конфигурации начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="79401-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="79401-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="79401-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="79401-127">Определяет частоту (в минутах), с которой работает Chef-служба.</span><span class="sxs-lookup"><span data-stu-id="79401-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="79401-128">Если вы не хотите, чтобы Chef-служба была установлена на виртуальной машине Azure, установите для этого поля значение 0.</span><span class="sxs-lookup"><span data-stu-id="79401-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="79401-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="79401-129">-ChefServerUrl</span></span>
<span data-ttu-id="79401-130">Указывает ссылку на сервер Chef в виде URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="79401-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="79401-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="79401-131">-ClientRb</span></span>
<span data-ttu-id="79401-132">Указывает полный путь к Chef Client. RB.</span><span class="sxs-lookup"><span data-stu-id="79401-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="79401-133">-Демон</span><span class="sxs-lookup"><span data-stu-id="79401-133">-Daemon</span></span>
<span data-ttu-id="79401-134">Настраивает службу Chef-Client для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="79401-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="79401-135">Платформа узла должна быть Windows.</span><span class="sxs-lookup"><span data-stu-id="79401-135">The node platform should be Windows.</span></span>
<span data-ttu-id="79401-136">Разрешенные варианты: "нет", "служба" и "задача".</span><span class="sxs-lookup"><span data-stu-id="79401-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="79401-137">None — в настоящее время служба Chef-клиента не будет настроена как служба.</span><span class="sxs-lookup"><span data-stu-id="79401-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="79401-138">Служба — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="79401-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="79401-139">задача — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве задачи secheduled.</span><span class="sxs-lookup"><span data-stu-id="79401-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-140">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="79401-140">-JsonAttribute</span></span>
<span data-ttu-id="79401-141">Строка JSON, добавляемая в первый запуск Chef-Client.</span><span class="sxs-lookup"><span data-stu-id="79401-141">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="79401-142">Например,-JsonAttribute ' {"foo": "отрезок"} "</span><span class="sxs-lookup"><span data-stu-id="79401-142">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="79401-143">-Linux</span><span class="sxs-lookup"><span data-stu-id="79401-143">-Linux</span></span>
<span data-ttu-id="79401-144">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="79401-144">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="79401-145">-Location</span><span class="sxs-lookup"><span data-stu-id="79401-145">-Location</span></span>
<span data-ttu-id="79401-146">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="79401-146">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79401-147">-Name</span></span>
<span data-ttu-id="79401-148">Указывает имя расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="79401-148">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-149">-Название_организации</span><span class="sxs-lookup"><span data-stu-id="79401-149">-OrganizationName</span></span>
<span data-ttu-id="79401-150">Указывает название организации для расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="79401-150">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="79401-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79401-151">-ResourceGroupName</span></span>
<span data-ttu-id="79401-152">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="79401-152">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-153">-RunList</span><span class="sxs-lookup"><span data-stu-id="79401-153">-RunList</span></span>
<span data-ttu-id="79401-154">Указывает список выполнения для узла Chef.</span><span class="sxs-lookup"><span data-stu-id="79401-154">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="79401-155">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="79401-155">-Secret</span></span>
<span data-ttu-id="79401-156">Ключ шифрования, используемый для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="79401-156">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="79401-157">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="79401-157">-SecretFile</span></span>
<span data-ttu-id="79401-158">Путь к файлу, содержащему ключ шифрования, который используется для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="79401-158">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="79401-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="79401-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="79401-160">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="79401-160">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-161">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="79401-161">-ValidationClientName</span></span>
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

### <span data-ttu-id="79401-162">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="79401-162">-ValidationPem</span></span>
<span data-ttu-id="79401-163">Задает путь к файлу проверяющего элемента управления Chef. PEM</span><span class="sxs-lookup"><span data-stu-id="79401-163">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="79401-164">-VMName</span><span class="sxs-lookup"><span data-stu-id="79401-164">-VMName</span></span>
<span data-ttu-id="79401-165">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="79401-165">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="79401-166">Этот командлет добавляет расширение Chef для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="79401-166">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79401-167">-Windows</span><span class="sxs-lookup"><span data-stu-id="79401-167">-Windows</span></span>
<span data-ttu-id="79401-168">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="79401-168">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="79401-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79401-169">-Confirm</span></span>
<span data-ttu-id="79401-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79401-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79401-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79401-171">-WhatIf</span></span>
<span data-ttu-id="79401-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79401-172">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="79401-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79401-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79401-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79401-174">CommonParameters</span></span>
<span data-ttu-id="79401-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79401-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79401-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79401-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79401-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79401-177">INPUTS</span></span>

### <span data-ttu-id="79401-178">Ничего</span><span class="sxs-lookup"><span data-stu-id="79401-178">None</span></span>
<span data-ttu-id="79401-179">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="79401-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79401-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79401-180">OUTPUTS</span></span>

## <span data-ttu-id="79401-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="79401-181">NOTES</span></span>

## <span data-ttu-id="79401-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79401-182">RELATED LINKS</span></span>

[<span data-ttu-id="79401-183">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="79401-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="79401-184">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="79401-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
