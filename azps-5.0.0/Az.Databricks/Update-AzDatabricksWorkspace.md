---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312803"
---
# <span data-ttu-id="d7ddd-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7ddd-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="d7ddd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ddd-103">Обновляет рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-103">Updates a workspace.</span></span>

## <span data-ttu-id="d7ddd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7ddd-104">SYNTAX</span></span>

### <span data-ttu-id="d7ddd-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7ddd-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7ddd-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7ddd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d7ddd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ddd-108">Обновляет рабочую область.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-108">Updates a workspace.</span></span>

## <span data-ttu-id="d7ddd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ddd-110">Пример 1: обновление тегов рабочей области "кирпичные данных"</span><span class="sxs-lookup"><span data-stu-id="d7ddd-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="d7ddd-111">Эта команда обновляет теги рабочей области модуля данных.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="d7ddd-112">Пример 2: Включение шифрования в рабочей области модуля данных</span><span class="sxs-lookup"><span data-stu-id="d7ddd-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="d7ddd-113">Включение шифрования в рабочей области для модуля "набор" выполняет три действия.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="d7ddd-114">Обновите рабочую область, указав `-PrepareEncryption` (если она не была создана).</span><span class="sxs-lookup"><span data-stu-id="d7ddd-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="d7ddd-115">Найдите `StorageAccountIdentityPrincipalId` в выходных данных последнего шага.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="d7ddd-116">Предоставление участнику разрешений на получение ключа.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="d7ddd-117">Обновите рабочую область еще раз, чтобы заполнить сведения о ключе шифрования:</span><span class="sxs-lookup"><span data-stu-id="d7ddd-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="d7ddd-118">Пример 3: отключение шифрования в рабочей области «кирпичные фрагменты»</span><span class="sxs-lookup"><span data-stu-id="d7ddd-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="d7ddd-119">Чтобы отключить шифрование, просто задайте `-EncryptionKeySource` значение `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="d7ddd-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="d7ddd-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-120">PARAMETERS</span></span>

### <span data-ttu-id="d7ddd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ddd-121">-AsJob</span></span>
<span data-ttu-id="d7ddd-122">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d7ddd-122">Run the command as a job</span></span>

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

### <span data-ttu-id="d7ddd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ddd-123">-DefaultProfile</span></span>
<span data-ttu-id="d7ddd-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7ddd-125">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="d7ddd-125">-EncryptionKeyName</span></span>
<span data-ttu-id="d7ddd-126">Имя ключа хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-126">The name of Key Vault key.</span></span>

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

### <span data-ttu-id="d7ddd-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="d7ddd-127">-EncryptionKeySource</span></span>
<span data-ttu-id="d7ddd-128">KeySource шифрования (поставщик).</span><span class="sxs-lookup"><span data-stu-id="d7ddd-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="d7ddd-129">Возможные значения (без учета регистра): Default, Microsoft. Keyvault</span><span class="sxs-lookup"><span data-stu-id="d7ddd-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="d7ddd-130">-EncryptionKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d7ddd-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="d7ddd-131">Универсальный код ресурса (DNS-имя) для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-131">The URI (DNS name) of the Key Vault.</span></span>

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

### <span data-ttu-id="d7ddd-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="d7ddd-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="d7ddd-133">Версия ключа KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-133">The version of KeyVault key.</span></span>

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

### <span data-ttu-id="d7ddd-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7ddd-134">-InputObject</span></span>
<span data-ttu-id="d7ddd-135">Параметр удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-135">Identity parameter.</span></span>
<span data-ttu-id="d7ddd-136">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7ddd-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7ddd-137">-Name</span></span>
<span data-ttu-id="d7ddd-138">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-138">The name of the workspace.</span></span>

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

### <span data-ttu-id="d7ddd-139">-Wait</span><span class="sxs-lookup"><span data-stu-id="d7ddd-139">-NoWait</span></span>
<span data-ttu-id="d7ddd-140">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d7ddd-140">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d7ddd-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="d7ddd-141">-PrepareEncryption</span></span>
<span data-ttu-id="d7ddd-142">Подготовьте рабочую область к шифрованию.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="d7ddd-143">Включает управляемое удостоверение для управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-143">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="d7ddd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ddd-144">-ResourceGroupName</span></span>
<span data-ttu-id="d7ddd-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-145">The name of the resource group.</span></span>
<span data-ttu-id="d7ddd-146">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-146">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7ddd-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7ddd-147">-SubscriptionId</span></span>
<span data-ttu-id="d7ddd-148">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-148">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7ddd-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="d7ddd-149">-Tag</span></span>
<span data-ttu-id="d7ddd-150">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-150">Resource tags.</span></span>

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

### <span data-ttu-id="d7ddd-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7ddd-151">-Confirm</span></span>
<span data-ttu-id="d7ddd-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ddd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ddd-153">-WhatIf</span></span>
<span data-ttu-id="d7ddd-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ddd-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ddd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ddd-156">CommonParameters</span></span>
<span data-ttu-id="d7ddd-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ddd-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7ddd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ddd-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7ddd-159">INPUTS</span></span>

### <span data-ttu-id="d7ddd-160">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="d7ddd-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="d7ddd-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-161">OUTPUTS</span></span>

### <span data-ttu-id="d7ddd-162">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7ddd-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="d7ddd-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7ddd-163">NOTES</span></span>

<span data-ttu-id="d7ddd-164">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-164">ALIASES</span></span>

<span data-ttu-id="d7ddd-165">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7ddd-166">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7ddd-167">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7ddd-168">INPUTOBJECT <IDatabricksIdentity> : параметр Identity.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="d7ddd-169">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d7ddd-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7ddd-170">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="d7ddd-171">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7ddd-172">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7ddd-173">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7ddd-174">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d7ddd-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="d7ddd-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7ddd-175">RELATED LINKS</span></span>

