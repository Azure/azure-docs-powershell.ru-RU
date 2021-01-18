---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516914"
---
# <span data-ttu-id="559e0-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="559e0-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="559e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="559e0-102">SYNOPSIS</span></span>
<span data-ttu-id="559e0-103">Обновляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="559e0-103">Updates a workspace.</span></span>

## <span data-ttu-id="559e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="559e0-104">SYNTAX</span></span>

### <span data-ttu-id="559e0-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="559e0-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="559e0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="559e0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="559e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="559e0-107">DESCRIPTION</span></span>
<span data-ttu-id="559e0-108">Обновляет рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="559e0-108">Updates a workspace.</span></span>

## <span data-ttu-id="559e0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="559e0-109">EXAMPLES</span></span>

### <span data-ttu-id="559e0-110">Пример 1. Обновление тегов рабочей области Datab ветвей</span><span class="sxs-lookup"><span data-stu-id="559e0-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="559e0-111">Эта команда обновляет теги рабочей области Datab ветвей.</span><span class="sxs-lookup"><span data-stu-id="559e0-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="559e0-112">Пример 2. Включить шифрование в рабочей области Databspaces</span><span class="sxs-lookup"><span data-stu-id="559e0-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="559e0-113">Включение шифрования в рабочей области Datab в рабочей области состоит из трех этапов:</span><span class="sxs-lookup"><span data-stu-id="559e0-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="559e0-114">Обновление рабочей области `-PrepareEncryption` (если она не была создана).</span><span class="sxs-lookup"><span data-stu-id="559e0-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="559e0-115">Результаты `StorageAccountIdentityPrincipalId` последнего шага.</span><span class="sxs-lookup"><span data-stu-id="559e0-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="559e0-116">Предоставить основные разрешения для основного.</span><span class="sxs-lookup"><span data-stu-id="559e0-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="559e0-117">Еще раз обновите рабочее пространство, чтобы в нем появилась информация о ключе шифрования.</span><span class="sxs-lookup"><span data-stu-id="559e0-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="559e0-118">Пример 3. Отключение шифрования в рабочей области Databspaces</span><span class="sxs-lookup"><span data-stu-id="559e0-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="559e0-119">Чтобы отключить шифрование, просто установите `-EncryptionKeySource` для этого нужное. `'Default'`</span><span class="sxs-lookup"><span data-stu-id="559e0-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="559e0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="559e0-120">PARAMETERS</span></span>

### <span data-ttu-id="559e0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="559e0-121">-AsJob</span></span>
<span data-ttu-id="559e0-122">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="559e0-122">Run the command as a job</span></span>

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

### <span data-ttu-id="559e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559e0-123">-DefaultProfile</span></span>
<span data-ttu-id="559e0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="559e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="559e0-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="559e0-125">-EncryptionKeyName</span></span>
<span data-ttu-id="559e0-126">Имя ключа сейфа.</span><span class="sxs-lookup"><span data-stu-id="559e0-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="559e0-127">-EncryptionKeySource</span></span>
<span data-ttu-id="559e0-128">Ключ шифрования (provider).</span><span class="sxs-lookup"><span data-stu-id="559e0-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="559e0-129">Возможные значения (без учета деления): Default, Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="559e0-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="559e0-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="559e0-131">URI (имя DNS) хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="559e0-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="559e0-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="559e0-133">Версия ключа KeyVault.</span><span class="sxs-lookup"><span data-stu-id="559e0-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="559e0-134">-InputObject</span></span>
<span data-ttu-id="559e0-135">Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="559e0-135">Identity parameter.</span></span>
<span data-ttu-id="559e0-136">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="559e0-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="559e0-137">-Name</span></span>
<span data-ttu-id="559e0-138">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="559e0-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="559e0-139">-NoWait</span></span>
<span data-ttu-id="559e0-140">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="559e0-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="559e0-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="559e0-141">-PrepareEncryption</span></span>
<span data-ttu-id="559e0-142">Подготовьте рабочее пространство для шифрования.</span><span class="sxs-lookup"><span data-stu-id="559e0-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="559e0-143">Включает управляемое удостоверение для учетной записи управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="559e0-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="559e0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="559e0-144">-ResourceGroupName</span></span>
<span data-ttu-id="559e0-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="559e0-145">The name of the resource group.</span></span>
<span data-ttu-id="559e0-146">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="559e0-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="559e0-147">-SubscriptionId</span></span>
<span data-ttu-id="559e0-148">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="559e0-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="559e0-149">-Tag</span></span>
<span data-ttu-id="559e0-150">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="559e0-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e0-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="559e0-151">-Confirm</span></span>
<span data-ttu-id="559e0-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="559e0-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="559e0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559e0-153">-WhatIf</span></span>
<span data-ttu-id="559e0-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="559e0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="559e0-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="559e0-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="559e0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559e0-156">CommonParameters</span></span>
<span data-ttu-id="559e0-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559e0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559e0-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="559e0-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559e0-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="559e0-159">INPUTS</span></span>

### <span data-ttu-id="559e0-160">Microsoft.Azure.PowerShell.Cmdlets.Datab ветвей.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="559e0-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="559e0-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="559e0-161">OUTPUTS</span></span>

### <span data-ttu-id="559e0-162">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="559e0-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="559e0-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="559e0-163">NOTES</span></span>

<span data-ttu-id="559e0-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="559e0-164">ALIASES</span></span>

<span data-ttu-id="559e0-165">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="559e0-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="559e0-166">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="559e0-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="559e0-167">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="559e0-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="559e0-168">INPUTOBJECT <IDatabricksIdentity> : Параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="559e0-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="559e0-169">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="559e0-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="559e0-170">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="559e0-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="559e0-171">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="559e0-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="559e0-172">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="559e0-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="559e0-173">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="559e0-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="559e0-174">`[WorkspaceName <String>]`: имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="559e0-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="559e0-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="559e0-175">RELATED LINKS</span></span>

