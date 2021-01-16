---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509033"
---
# <span data-ttu-id="fff5f-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fff5f-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="fff5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fff5f-103">Добавляет расширение Для ветвей на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fff5f-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="fff5f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fff5f-104">SYNTAX</span></span>

### <span data-ttu-id="fff5f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="fff5f-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fff5f-106">Windows</span><span class="sxs-lookup"><span data-stu-id="fff5f-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff5f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fff5f-107">DESCRIPTION</span></span>
<span data-ttu-id="fff5f-108">Cmdlet **Set-AzVMChefExtension** добавит расширение "Вален" на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fff5f-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="fff5f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fff5f-109">EXAMPLES</span></span>

### <span data-ttu-id="fff5f-110">Пример 1. Добавление расширения "Валенка" на виртуальную машину Windows</span><span class="sxs-lookup"><span data-stu-id="fff5f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="fff5f-111">Эта команда добавляет расширение к виртуальной машине Windows с именем WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="fff5f-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="fff5f-112">Когда начнется виртуальная машину, Она будет запускаться на виртуальной машине, чтобы запустить Apache.</span><span class="sxs-lookup"><span data-stu-id="fff5f-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="fff5f-113">Пример 2. Добавление расширения "Разработчик" на виртуальную машину Linux</span><span class="sxs-lookup"><span data-stu-id="fff5f-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="fff5f-114">Эта команда добавляет расширение Вайла на виртуальную машину Linux с именем LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="fff5f-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="fff5f-115">Когда начнется виртуальная машину, Она будет запускаться на виртуальной машине, чтобы запустить Apache.</span><span class="sxs-lookup"><span data-stu-id="fff5f-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="fff5f-116">Пример 3. Добавление расширения "Валенка" на виртуальную машину Windows с вариантами bootstrap</span><span class="sxs-lookup"><span data-stu-id="fff5f-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="fff5f-117">Эта команда добавляет расширение "Данный" на виртуальную машину Windows с именем WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="fff5f-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="fff5f-118">Когда начнется виртуальная машину, Она будет запускаться на виртуальной машине, чтобы запустить Apache.</span><span class="sxs-lookup"><span data-stu-id="fff5f-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="fff5f-119">После загрузки виртуальная машину ссылается на bootstrapOptions, указанные в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="fff5f-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="fff5f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff5f-120">PARAMETERS</span></span>

### <span data-ttu-id="fff5f-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fff5f-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="fff5f-122">-BootstrapOptions</span></span>
<span data-ttu-id="fff5f-123">Определяет параметры конфигурации в параметре client_rb настройки.</span><span class="sxs-lookup"><span data-stu-id="fff5f-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="fff5f-124">-BootstrapVersion</span></span>
<span data-ttu-id="fff5f-125">Определяет версию конфигурации bootstrap.</span><span class="sxs-lookup"><span data-stu-id="fff5f-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-126">-DaemonInterval</span><span class="sxs-lookup"><span data-stu-id="fff5f-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="fff5f-127">Определяет частоту работы службы (в минутах).</span><span class="sxs-lookup"><span data-stu-id="fff5f-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="fff5f-128">Если вы не хотите, чтобы на VM Azure была установлена разная служба, в этом поле установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="fff5f-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-129">-2016Url</span><span class="sxs-lookup"><span data-stu-id="fff5f-129">-ChefServerUrl</span></span>
<span data-ttu-id="fff5f-130">Указывает ссылку на сервер в качестве URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="fff5f-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="fff5f-131">-ClientRb</span></span>
<span data-ttu-id="fff5f-132">Указывает полный путь к клиенту", который является "Разбит".</span><span class="sxs-lookup"><span data-stu-id="fff5f-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="fff5f-133">-Daemon</span></span>
<span data-ttu-id="fff5f-134">Настраивает клиентскую службу для неотвеченного выполнения.</span><span class="sxs-lookup"><span data-stu-id="fff5f-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="fff5f-135">Платформа узла должна быть Windows.</span><span class="sxs-lookup"><span data-stu-id="fff5f-135">The node platform should be Windows.</span></span>
<span data-ttu-id="fff5f-136">Разрешенные параметры: "нет", "служба" и "задача".</span><span class="sxs-lookup"><span data-stu-id="fff5f-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="fff5f-137">нет. В настоящее время не позволяет настроить клиентскую службу как службу.</span><span class="sxs-lookup"><span data-stu-id="fff5f-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="fff5f-138">— настраивает клиент в качестве службы для автоматического запуска в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fff5f-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="fff5f-139">— настраивает клиент для автоматического запуска в фоновом режиме в качестве запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="fff5f-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff5f-140">-DefaultProfile</span></span>
<span data-ttu-id="fff5f-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fff5f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="fff5f-142">-JsonAttribute</span></span>
<span data-ttu-id="fff5f-143">Строка JSON, которая будет добавлена в первый запуск клиент-клиента.</span><span class="sxs-lookup"><span data-stu-id="fff5f-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="fff5f-144">Например: -JsonAttribute '{"foo" : "bar"}"</span><span class="sxs-lookup"><span data-stu-id="fff5f-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="fff5f-145">-Linux</span></span>
<span data-ttu-id="fff5f-146">Указывает на то, что этот cmdlet создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="fff5f-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-147">-Location</span><span class="sxs-lookup"><span data-stu-id="fff5f-147">-Location</span></span>
<span data-ttu-id="fff5f-148">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fff5f-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-149">-Name</span><span class="sxs-lookup"><span data-stu-id="fff5f-149">-Name</span></span>
<span data-ttu-id="fff5f-150">Указывает имя расширения "Валенка".</span><span class="sxs-lookup"><span data-stu-id="fff5f-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fff5f-151">-NoWait</span></span>
<span data-ttu-id="fff5f-152">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="fff5f-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="fff5f-153">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="fff5f-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="fff5f-154">-OrganizationName</span></span>
<span data-ttu-id="fff5f-155">Указывает название организации расширения "Фамилия".</span><span class="sxs-lookup"><span data-stu-id="fff5f-155">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff5f-156">-ResourceGroupName</span></span>
<span data-ttu-id="fff5f-157">Имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fff5f-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="fff5f-158">-RunList</span></span>
<span data-ttu-id="fff5f-159">Определяет список запуска узла ветвей.</span><span class="sxs-lookup"><span data-stu-id="fff5f-159">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-160">-Секретная</span><span class="sxs-lookup"><span data-stu-id="fff5f-160">-Secret</span></span>
<span data-ttu-id="fff5f-161">Ключ шифрования, используемый для шифрования и расшифровки значений элементов в пакете данных.</span><span class="sxs-lookup"><span data-stu-id="fff5f-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="fff5f-162">-SecretFile</span></span>
<span data-ttu-id="fff5f-163">Путь к файлу, который содержит ключ шифрования, используемый для шифрования и расшифровки значений элементов в пакете данных.</span><span class="sxs-lookup"><span data-stu-id="fff5f-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fff5f-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="fff5f-165">Определяет версию расширения, используемого для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fff5f-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="fff5f-166">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="fff5f-167">-ValidationPem</span></span>
<span data-ttu-id="fff5f-168">Указывает путь к PEM-файлу validator .pem</span><span class="sxs-lookup"><span data-stu-id="fff5f-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="fff5f-169">-VMName</span></span>
<span data-ttu-id="fff5f-170">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fff5f-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fff5f-171">Этот cmdlet добавит расширение "Валенка" для виртуальной машины, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fff5f-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="fff5f-172">-Windows</span></span>
<span data-ttu-id="fff5f-173">Указывает на то, что этот cmdlet создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="fff5f-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fff5f-174">-Confirm</span></span>
<span data-ttu-id="fff5f-175">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff5f-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff5f-176">-WhatIf</span></span>
<span data-ttu-id="fff5f-177">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff5f-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fff5f-178">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fff5f-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff5f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff5f-179">CommonParameters</span></span>
<span data-ttu-id="fff5f-180">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff5f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff5f-181">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff5f-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff5f-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fff5f-182">INPUTS</span></span>

### <span data-ttu-id="fff5f-183">System.String</span><span class="sxs-lookup"><span data-stu-id="fff5f-183">System.String</span></span>

### <span data-ttu-id="fff5f-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fff5f-184">System.Boolean</span></span>

## <span data-ttu-id="fff5f-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fff5f-185">OUTPUTS</span></span>

### <span data-ttu-id="fff5f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fff5f-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fff5f-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fff5f-187">NOTES</span></span>

## <span data-ttu-id="fff5f-188">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fff5f-188">RELATED LINKS</span></span>

[<span data-ttu-id="fff5f-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fff5f-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="fff5f-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="fff5f-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
