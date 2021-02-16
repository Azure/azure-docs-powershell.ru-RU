---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211876"
---
# <span data-ttu-id="0ab49-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="0ab49-101">Update-AzCloudService</span></span>

## <span data-ttu-id="0ab49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab49-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab49-103">Создайте или обновйте облачную службу.</span><span class="sxs-lookup"><span data-stu-id="0ab49-103">Create or update a cloud service.</span></span>
<span data-ttu-id="0ab49-104">Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="0ab49-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ab49-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ab49-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ab49-106">DESCRIPTION</span></span>
<span data-ttu-id="0ab49-107">Создайте или обновйте облачную службу.</span><span class="sxs-lookup"><span data-stu-id="0ab49-107">Create or update a cloud service.</span></span>
<span data-ttu-id="0ab49-108">Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="0ab49-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ab49-109">EXAMPLES</span></span>

### <span data-ttu-id="0ab49-110">Пример 1. Добавление расширения RDP в существующую облачную службу</span><span class="sxs-lookup"><span data-stu-id="0ab49-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="0ab49-111">Над набором команд добавляется расширение RDP к уже существующей облачной службе ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="0ab49-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="0ab49-112">Пример 2. Удаление всех расширений из облачной службы</span><span class="sxs-lookup"><span data-stu-id="0ab49-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="0ab49-113">Набор команд выше удаляет все расширения из существующей облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="0ab49-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="0ab49-114">Пример 3. Удаление расширения RDP из облачной службы</span><span class="sxs-lookup"><span data-stu-id="0ab49-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="0ab49-115">Над набором команд удаляется расширение RDP из существующей облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="0ab49-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="0ab49-116">Пример 4. Scale-Out и Scale-In роли</span><span class="sxs-lookup"><span data-stu-id="0ab49-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="0ab49-117">Над набором команд показано, как масштабировать и масштабировать количество экземпляров ролей для облачной службы ContosoCS, которая принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="0ab49-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="0ab49-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ab49-118">PARAMETERS</span></span>

### <span data-ttu-id="0ab49-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ab49-119">-AsJob</span></span>
<span data-ttu-id="0ab49-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0ab49-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0ab49-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab49-121">-DefaultProfile</span></span>
<span data-ttu-id="0ab49-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab49-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab49-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ab49-123">-InputObject</span></span>
<span data-ttu-id="0ab49-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0ab49-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab49-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ab49-125">-NoWait</span></span>
<span data-ttu-id="0ab49-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0ab49-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ab49-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab49-127">-Parameter</span></span>
<span data-ttu-id="0ab49-128">Описание облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-128">Describes the cloud service.</span></span>
<span data-ttu-id="0ab49-129">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств PARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0ab49-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab49-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ab49-130">-Confirm</span></span>
<span data-ttu-id="0ab49-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab49-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab49-132">-WhatIf</span></span>
<span data-ttu-id="0ab49-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ab49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ab49-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ab49-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab49-135">CommonParameters</span></span>
<span data-ttu-id="0ab49-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab49-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ab49-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab49-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ab49-138">INPUTS</span></span>

### <span data-ttu-id="0ab49-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="0ab49-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="0ab49-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="0ab49-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="0ab49-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ab49-141">OUTPUTS</span></span>

### <span data-ttu-id="0ab49-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="0ab49-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="0ab49-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ab49-143">NOTES</span></span>

<span data-ttu-id="0ab49-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0ab49-144">ALIASES</span></span>

<span data-ttu-id="0ab49-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0ab49-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ab49-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0ab49-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ab49-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ab49-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ab49-148">INPUTOBJECT <ICloudServiceIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0ab49-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ab49-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0ab49-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="0ab49-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ab49-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0ab49-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="0ab49-152">`[RoleInstanceName <String>]`: Имя экземпляра роли.</span><span class="sxs-lookup"><span data-stu-id="0ab49-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="0ab49-153">`[RoleName <String>]`: Название роли.</span><span class="sxs-lookup"><span data-stu-id="0ab49-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="0ab49-154">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab49-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0ab49-155">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0ab49-156">`[UpdateDomain <Int32?>]`: Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="0ab49-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="0ab49-157">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="0ab49-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="0ab49-158">PARAMETER <ICloudService> : Описание облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="0ab49-159">`Location <String>`: расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ab49-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="0ab49-160">`[Configuration <String>]`Определяет конфигурацию службы XML (CSCFG) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="0ab49-161">`[ConfigurationUrl <String>]`: указывает URL-адрес, который ссылается на расположение конфигурации службы в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="0ab49-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="0ab49-162">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="0ab49-163">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="0ab49-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="0ab49-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Описание профиля расширения облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="0ab49-165">`[Extension <IExtension[]>]`: Список расширений для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="0ab49-166">`[AutoUpgradeMinorVersion <Boolean?>]`. Явным образом укажите, может ли платформа автоматически обновлять TypeHandlerVersion до более мелких версий, когда они станут доступны.</span><span class="sxs-lookup"><span data-stu-id="0ab49-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="0ab49-167">`[ForceUpdateTag <String>]`: примените к тегу предоставленные общедоступные и защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="0ab49-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="0ab49-168">Изменение значения тега позволяет повторно запускать расширение без изменения общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="0ab49-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="0ab49-169">Если параметр forceUpdateTag не изменился, обработник по-прежнему будет применять обновления общедоступных или защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="0ab49-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="0ab49-170">Если ни принудительное изменение параметра,ни каких-либо из общедоступных или защищенных параметров не изменилось, расширение будет перенаправляться в экземпляр роли с одинаковым номером последовательности и будет возможно повторное внедрение.</span><span class="sxs-lookup"><span data-stu-id="0ab49-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="0ab49-171">`[Name <String>]`: имя расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="0ab49-172">`[ProtectedSetting <String>]`: Защищенные параметры расширения, которые шифруются перед его отправлением в экземпляр роли.</span><span class="sxs-lookup"><span data-stu-id="0ab49-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="0ab49-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0ab49-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="0ab49-174">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="0ab49-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="0ab49-175">`[RolesAppliedTo <String[]>]`: Необязательный список ролей для применения этого расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="0ab49-176">Если свойство не указано или указано "\*", расширение применяется для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="0ab49-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="0ab49-177">`[Setting <String>]`: общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="0ab49-178">Для расширений JSON это параметры JSON.</span><span class="sxs-lookup"><span data-stu-id="0ab49-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="0ab49-179">Для расширения XML (например, RDP) это параметр XML для расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="0ab49-180">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0ab49-181">`[Type <String>]`: тип расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="0ab49-182">`[TypeHandlerVersion <String>]`: Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="0ab49-183">Определяет версию расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-183">Specifies the version of the extension.</span></span> <span data-ttu-id="0ab49-184">Если этот элемент не указан или в качестве значения используется звездочка (\*), используется последняя версия расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="0ab49-185">Если задан номер основной версии и звездочка как дополнительный номер версии (X.), будет выбрана последняя дополнительный версия указанной основной версии.</span><span class="sxs-lookup"><span data-stu-id="0ab49-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="0ab49-186">Если указан основной и второстепенный номер версии (X.Y), будет выбрана конкретная версия расширения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="0ab49-187">Если указана версия, для экземпляра роли выполняется автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="0ab49-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="0ab49-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Профиль сети для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="0ab49-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`Список конфигураций балансиров нагрузки для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="0ab49-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Список IP-адресов</span><span class="sxs-lookup"><span data-stu-id="0ab49-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="0ab49-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="0ab49-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="0ab49-192">`[PrivateIPAddress <String>]`: личный IP-адрес, на который ссылается облачная служба.</span><span class="sxs-lookup"><span data-stu-id="0ab49-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="0ab49-193">`[PublicIPAddressId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="0ab49-194">`[SubnetId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0ab49-195">`[Name <String>]`: Название ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="0ab49-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="0ab49-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="0ab49-197">`[Id <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="0ab49-198">`[OSProfile <ICloudServiceOSProfile>]`: описание профиля ОС для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="0ab49-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Набор сертификатов, которые нужно установить на экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="0ab49-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="0ab49-200">`[SourceVaultId <String>]`: ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="0ab49-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="0ab49-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: список ссылок на основные хранилища в SourceVault, которые содержат сертификаты.</span><span class="sxs-lookup"><span data-stu-id="0ab49-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="0ab49-202">`[CertificateUrl <String>]`. Это URL-адрес сертификата, который был выложен в хранилище ключей в качестве секретного.</span><span class="sxs-lookup"><span data-stu-id="0ab49-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="0ab49-203">`[PackageUrl <String>]`: указывает URL-адрес, который ссылается на расположение пакета обслуживания в службе BLOB-бизнес.</span><span class="sxs-lookup"><span data-stu-id="0ab49-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="0ab49-204">URL-адрес пакета обслуживания может быть URI подписи общего доступа (SAS) из любой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0ab49-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="0ab49-205">Это свойство является свойством только для записи и не возвращается при звонках GET.</span><span class="sxs-lookup"><span data-stu-id="0ab49-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="0ab49-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Описание профиля роли для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="0ab49-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: Список ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="0ab49-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="0ab49-208">`[Name <String>]`: название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ab49-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="0ab49-209">`[SkuCapacity <Int64?>]`Определяет количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="0ab49-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="0ab49-210">`[SkuName <String>]`: название SKU.</span><span class="sxs-lookup"><span data-stu-id="0ab49-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="0ab49-211">ПРИМЕЧАНИЕ. Если новый SKU не поддерживается на оборудовании, наемное облачным сервисом, необходимо удалить и воссоздать облачную службу или вернуться к старым SKU.</span><span class="sxs-lookup"><span data-stu-id="0ab49-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="0ab49-212">`[SkuTier <String>]`: уровень облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="0ab49-213">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0ab49-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="0ab49-214">**Стандартный**</span><span class="sxs-lookup"><span data-stu-id="0ab49-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="0ab49-215">**Базовая**</span><span class="sxs-lookup"><span data-stu-id="0ab49-215">**Basic**</span></span>
  - <span data-ttu-id="0ab49-216">`[StartCloudService <Boolean?>]`: (Необязательно) Указывает, следует ли запускать облачную службу сразу после ее создания.</span><span class="sxs-lookup"><span data-stu-id="0ab49-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="0ab49-217">Значение по `true` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="0ab49-217">The default value is `true`.</span></span>         <span data-ttu-id="0ab49-218">Если этот код ложный, модель обслуживания по-прежнему развертывается, но не сразу же запустится.</span><span class="sxs-lookup"><span data-stu-id="0ab49-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="0ab49-219">Вместо этого служба будет иметь poweredOff, пока вы не позвоните в службу "Начните", и она будет запущена.</span><span class="sxs-lookup"><span data-stu-id="0ab49-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="0ab49-220">С развернутой службы по-прежнему взимается плата, даже если она отключена.</span><span class="sxs-lookup"><span data-stu-id="0ab49-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="0ab49-221">`[Tag <ICloudServiceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ab49-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0ab49-222">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="0ab49-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0ab49-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`Режим обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="0ab49-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="0ab49-224">При развертывании службы для обновления доменов выделяются экземпляры ролей.</span><span class="sxs-lookup"><span data-stu-id="0ab49-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="0ab49-225">Обновления можно за инициативой обновления вручную в каждом домене обновления или автоматически во всех доменах обновления.</span><span class="sxs-lookup"><span data-stu-id="0ab49-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="0ab49-226">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="0ab49-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="0ab49-227">**Авто**</span><span class="sxs-lookup"><span data-stu-id="0ab49-227">**Auto**</span></span><br /><br /><span data-ttu-id="0ab49-228">**Вручную**</span><span class="sxs-lookup"><span data-stu-id="0ab49-228">**Manual**</span></span> <br /><br /><span data-ttu-id="0ab49-229">**Одновременный**</span><span class="sxs-lookup"><span data-stu-id="0ab49-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="0ab49-230">Если не указано, по умолчанию задано значение "Авто". Чтобы применить обновление вручную, необходимо создать put UpdateDomain.</span><span class="sxs-lookup"><span data-stu-id="0ab49-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="0ab49-231">Если за установлено автоматическое обновление, обновление автоматически применяется к каждому домену обновления последовательно.</span><span class="sxs-lookup"><span data-stu-id="0ab49-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="0ab49-232">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ab49-232">RELATED LINKS</span></span>

