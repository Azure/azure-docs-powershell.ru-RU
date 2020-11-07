---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: 277790badbaeef02139034ffd32f639f90929133
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914897"
---
# <span data-ttu-id="21f9e-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="21f9e-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="21f9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="21f9e-103">Добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="21f9e-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21f9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21f9e-104">SYNTAX</span></span>

### <span data-ttu-id="21f9e-105">Linux</span><span class="sxs-lookup"><span data-stu-id="21f9e-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21f9e-106">Windows</span><span class="sxs-lookup"><span data-stu-id="21f9e-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21f9e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21f9e-107">DESCRIPTION</span></span>
<span data-ttu-id="21f9e-108">Командлет **Set-AzureVMChefExtension** добавляет расширение Chef на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="21f9e-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="21f9e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21f9e-109">EXAMPLES</span></span>

### <span data-ttu-id="21f9e-110">Пример 1: Добавление расширения Chef на виртуальную машину Windows</span><span class="sxs-lookup"><span data-stu-id="21f9e-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="21f9e-111">Эта команда добавляет расширение Chef на виртуальную машину Windows с именем WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="21f9e-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="21f9e-112">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="21f9e-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="21f9e-113">Пример 2: Добавление расширения Chef на виртуальную машину Linux</span><span class="sxs-lookup"><span data-stu-id="21f9e-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="21f9e-114">Эта команда добавляет расширение Chef на виртуальную машину Linux с именем LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="21f9e-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="21f9e-115">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="21f9e-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="21f9e-116">Пример 3: Добавление расширения Chef для виртуальной машины Windows с помощью параметров начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="21f9e-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="21f9e-117">Эта команда добавляет расширение Chef на виртуальную машину Windows с именем WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="21f9e-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="21f9e-118">При запуске виртуальной машины Chef загружает виртуальную машину для запуска Apache.</span><span class="sxs-lookup"><span data-stu-id="21f9e-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="21f9e-119">После начальной загрузки виртуальная машина ссылается на BootstrapOptions, указанный в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="21f9e-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="21f9e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21f9e-120">PARAMETERS</span></span>

### <span data-ttu-id="21f9e-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="21f9e-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="21f9e-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="21f9e-122">-BootstrapOptions</span></span>
<span data-ttu-id="21f9e-123">Задает параметры конфигурации в параметре client_rb.</span><span class="sxs-lookup"><span data-stu-id="21f9e-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="21f9e-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="21f9e-124">-BootstrapVersion</span></span>
<span data-ttu-id="21f9e-125">Задает версию конфигурации начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="21f9e-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="21f9e-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="21f9e-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="21f9e-127">Определяет частоту (в минутах), с которой работает Chef-служба.</span><span class="sxs-lookup"><span data-stu-id="21f9e-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="21f9e-128">Если вы не хотите, чтобы Chef-служба была установлена на виртуальной машине Azure, установите для этого поля значение 0.</span><span class="sxs-lookup"><span data-stu-id="21f9e-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="21f9e-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="21f9e-129">-ChefServerUrl</span></span>
<span data-ttu-id="21f9e-130">Указывает ссылку на сервер Chef в виде URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="21f9e-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="21f9e-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="21f9e-131">-ClientRb</span></span>
<span data-ttu-id="21f9e-132">Указывает полный путь к Chef Client. RB.</span><span class="sxs-lookup"><span data-stu-id="21f9e-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="21f9e-133">-Демон</span><span class="sxs-lookup"><span data-stu-id="21f9e-133">-Daemon</span></span>
<span data-ttu-id="21f9e-134">Настраивает службу Chef-Client для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="21f9e-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="21f9e-135">Платформа узла должна быть Windows.</span><span class="sxs-lookup"><span data-stu-id="21f9e-135">The node platform should be Windows.</span></span>
<span data-ttu-id="21f9e-136">Разрешенные варианты: "нет", "служба" и "задача".</span><span class="sxs-lookup"><span data-stu-id="21f9e-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="21f9e-137">None — в настоящее время служба Chef-клиента не будет настроена как служба.</span><span class="sxs-lookup"><span data-stu-id="21f9e-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="21f9e-138">Служба — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="21f9e-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="21f9e-139">задача — настраивает для клиента Chef автоматический запуск в фоновом режиме в качестве задачи secheduled.</span><span class="sxs-lookup"><span data-stu-id="21f9e-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="21f9e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f9e-140">-DefaultProfile</span></span>
<span data-ttu-id="21f9e-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21f9e-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f9e-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="21f9e-142">-JsonAttribute</span></span>
<span data-ttu-id="21f9e-143">Строка JSON, добавляемая в первый запуск Chef-Client.</span><span class="sxs-lookup"><span data-stu-id="21f9e-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="21f9e-144">Например,-JsonAttribute ' {"foo": "отрезок"} "</span><span class="sxs-lookup"><span data-stu-id="21f9e-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="21f9e-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="21f9e-145">-Linux</span></span>
<span data-ttu-id="21f9e-146">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="21f9e-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="21f9e-147">-Location</span><span class="sxs-lookup"><span data-stu-id="21f9e-147">-Location</span></span>
<span data-ttu-id="21f9e-148">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21f9e-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="21f9e-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21f9e-149">-Name</span></span>
<span data-ttu-id="21f9e-150">Указывает имя расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="21f9e-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="21f9e-151">-Название_организации</span><span class="sxs-lookup"><span data-stu-id="21f9e-151">-OrganizationName</span></span>
<span data-ttu-id="21f9e-152">Указывает название организации для расширения Chef.</span><span class="sxs-lookup"><span data-stu-id="21f9e-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="21f9e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f9e-153">-ResourceGroupName</span></span>
<span data-ttu-id="21f9e-154">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="21f9e-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="21f9e-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="21f9e-155">-RunList</span></span>
<span data-ttu-id="21f9e-156">Указывает список выполнения для узла Chef.</span><span class="sxs-lookup"><span data-stu-id="21f9e-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="21f9e-157">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="21f9e-157">-Secret</span></span>
<span data-ttu-id="21f9e-158">Ключ шифрования, используемый для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="21f9e-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="21f9e-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="21f9e-159">-SecretFile</span></span>
<span data-ttu-id="21f9e-160">Путь к файлу, содержащему ключ шифрования, который используется для шифрования и расшифровки значений элементов в контейнере данных.</span><span class="sxs-lookup"><span data-stu-id="21f9e-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="21f9e-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="21f9e-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="21f9e-162">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21f9e-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="21f9e-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="21f9e-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="21f9e-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="21f9e-164">-ValidationPem</span></span>
<span data-ttu-id="21f9e-165">Задает путь к файлу проверяющего элемента управления Chef. PEM</span><span class="sxs-lookup"><span data-stu-id="21f9e-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="21f9e-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="21f9e-166">-VMName</span></span>
<span data-ttu-id="21f9e-167">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="21f9e-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="21f9e-168">Этот командлет добавляет расширение Chef для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="21f9e-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="21f9e-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="21f9e-169">-Windows</span></span>
<span data-ttu-id="21f9e-170">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="21f9e-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="21f9e-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21f9e-171">-Confirm</span></span>
<span data-ttu-id="21f9e-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21f9e-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f9e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f9e-173">-WhatIf</span></span>
<span data-ttu-id="21f9e-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21f9e-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="21f9e-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21f9e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f9e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f9e-176">CommonParameters</span></span>
<span data-ttu-id="21f9e-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21f9e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f9e-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f9e-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f9e-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21f9e-179">INPUTS</span></span>

### <span data-ttu-id="21f9e-180">Ничего</span><span class="sxs-lookup"><span data-stu-id="21f9e-180">None</span></span>
<span data-ttu-id="21f9e-181">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="21f9e-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21f9e-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21f9e-182">OUTPUTS</span></span>

### <span data-ttu-id="21f9e-183">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="21f9e-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="21f9e-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="21f9e-184">NOTES</span></span>

## <span data-ttu-id="21f9e-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21f9e-185">RELATED LINKS</span></span>

[<span data-ttu-id="21f9e-186">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="21f9e-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="21f9e-187">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="21f9e-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
