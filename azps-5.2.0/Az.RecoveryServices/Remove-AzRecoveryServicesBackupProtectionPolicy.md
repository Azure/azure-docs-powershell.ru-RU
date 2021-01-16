---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329114"
---
# <span data-ttu-id="06951-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06951-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="06951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06951-102">SYNOPSIS</span></span>
<span data-ttu-id="06951-103">Удаляет политику защиты от резервного копирования из хранилища.</span><span class="sxs-lookup"><span data-stu-id="06951-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="06951-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06951-104">SYNTAX</span></span>

### <span data-ttu-id="06951-105">PolicyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06951-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06951-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="06951-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06951-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06951-107">DESCRIPTION</span></span>
<span data-ttu-id="06951-108">С **его учетом** удаляются политики резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="06951-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="06951-109">Перед удалением политики защиты от резервного копирования не должно быть связанных с ней элементов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="06951-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="06951-110">Прежде чем удалять политику, убедитесь, что каждый связанный элемент связан с какой-либо другой политикой.</span><span class="sxs-lookup"><span data-stu-id="06951-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="06951-111">Чтобы связать другую политику с элементом резервного копирования, используйте Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="06951-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="06951-112">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="06951-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="06951-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06951-113">EXAMPLES</span></span>

### <span data-ttu-id="06951-114">Пример 1. Удаление политики</span><span class="sxs-lookup"><span data-stu-id="06951-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="06951-115">Первая команда получает политику защиты резервного копирования с именем NewPolicy, а затем сохраняет ее в $Pol переменной.</span><span class="sxs-lookup"><span data-stu-id="06951-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="06951-116">Вторая команда удаляет объект политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="06951-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="06951-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="06951-117">Example 2</span></span>

<span data-ttu-id="06951-118">Удаляет политику защиты от резервного копирования из хранилища.</span><span class="sxs-lookup"><span data-stu-id="06951-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="06951-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="06951-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="06951-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06951-120">PARAMETERS</span></span>

### <span data-ttu-id="06951-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06951-121">-DefaultProfile</span></span>
<span data-ttu-id="06951-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06951-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06951-123">-Force</span><span class="sxs-lookup"><span data-stu-id="06951-123">-Force</span></span>
<span data-ttu-id="06951-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="06951-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06951-125">-Name</span><span class="sxs-lookup"><span data-stu-id="06951-125">-Name</span></span>
<span data-ttu-id="06951-126">Имя удаляемой политики защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="06951-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06951-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06951-127">-PassThru</span></span>
<span data-ttu-id="06951-128">Возвращает политику, которая будет удалена.</span><span class="sxs-lookup"><span data-stu-id="06951-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="06951-129">-Политика</span><span class="sxs-lookup"><span data-stu-id="06951-129">-Policy</span></span>
<span data-ttu-id="06951-130">Политика защиты от резервного копирования, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="06951-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="06951-131">Чтобы получить объект **BackupPolicy,** используйте Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="06951-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06951-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="06951-132">-VaultId</span></span>
<span data-ttu-id="06951-133">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="06951-133">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06951-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06951-134">-Confirm</span></span>
<span data-ttu-id="06951-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="06951-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06951-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06951-136">-WhatIf</span></span>
<span data-ttu-id="06951-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06951-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="06951-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06951-138">CommonParameters</span></span>
<span data-ttu-id="06951-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06951-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06951-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06951-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06951-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06951-141">INPUTS</span></span>

### <span data-ttu-id="06951-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="06951-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="06951-143">System.String</span><span class="sxs-lookup"><span data-stu-id="06951-143">System.String</span></span>

## <span data-ttu-id="06951-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06951-144">OUTPUTS</span></span>

### <span data-ttu-id="06951-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="06951-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="06951-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06951-146">NOTES</span></span>

## <span data-ttu-id="06951-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06951-147">RELATED LINKS</span></span>

[<span data-ttu-id="06951-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06951-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="06951-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06951-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="06951-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="06951-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


