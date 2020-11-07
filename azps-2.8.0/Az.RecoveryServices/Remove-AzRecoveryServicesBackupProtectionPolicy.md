---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905826"
---
# <span data-ttu-id="308b1-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="308b1-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="308b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="308b1-102">SYNOPSIS</span></span>
<span data-ttu-id="308b1-103">Удаление политики защиты резервных копий из хранилища.</span><span class="sxs-lookup"><span data-stu-id="308b1-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="308b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="308b1-104">SYNTAX</span></span>

### <span data-ttu-id="308b1-105">PolicyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="308b1-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="308b1-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="308b1-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="308b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="308b1-107">DESCRIPTION</span></span>
<span data-ttu-id="308b1-108">Командлет **Remove-AzRecoveryServicesBackupProtectionPolicy** удаляет политики резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="308b1-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="308b1-109">Прежде чем можно будет удалить политику защиты резервных копий, она не должна содержать ни одного связанного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="308b1-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="308b1-110">Перед удалением политики убедитесь, что все связанные элементы связаны с какой – либо другой политикой.</span><span class="sxs-lookup"><span data-stu-id="308b1-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="308b1-111">Чтобы связать другую политику с элементом резервной копии, используйте командлет Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="308b1-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="308b1-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="308b1-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="308b1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="308b1-113">EXAMPLES</span></span>

### <span data-ttu-id="308b1-114">Пример 1: Удаление политики</span><span class="sxs-lookup"><span data-stu-id="308b1-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="308b1-115">Первая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="308b1-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="308b1-116">Вторая команда удаляет объект политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="308b1-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="308b1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="308b1-117">PARAMETERS</span></span>

### <span data-ttu-id="308b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308b1-118">-DefaultProfile</span></span>
<span data-ttu-id="308b1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="308b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="308b1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="308b1-120">-Force</span></span>
<span data-ttu-id="308b1-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="308b1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="308b1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="308b1-122">-Name</span></span>
<span data-ttu-id="308b1-123">Задает имя удаляемой политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="308b1-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="308b1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="308b1-124">-PassThru</span></span>
<span data-ttu-id="308b1-125">Возврат политики для удаления.</span><span class="sxs-lookup"><span data-stu-id="308b1-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="308b1-126">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="308b1-126">-Policy</span></span>
<span data-ttu-id="308b1-127">Задает политику защиты резервного копирования, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="308b1-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="308b1-128">Чтобы получить объект **BackupPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="308b1-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="308b1-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="308b1-129">-VaultId</span></span>
<span data-ttu-id="308b1-130">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="308b1-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="308b1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="308b1-131">-Confirm</span></span>
<span data-ttu-id="308b1-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="308b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="308b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="308b1-133">-WhatIf</span></span>
<span data-ttu-id="308b1-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="308b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="308b1-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="308b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="308b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308b1-136">CommonParameters</span></span>
<span data-ttu-id="308b1-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="308b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308b1-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="308b1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308b1-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="308b1-139">INPUTS</span></span>

### <span data-ttu-id="308b1-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="308b1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="308b1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="308b1-141">System.String</span></span>

## <span data-ttu-id="308b1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="308b1-142">OUTPUTS</span></span>

### <span data-ttu-id="308b1-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="308b1-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="308b1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="308b1-144">NOTES</span></span>

## <span data-ttu-id="308b1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="308b1-145">RELATED LINKS</span></span>

[<span data-ttu-id="308b1-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="308b1-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="308b1-147">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="308b1-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="308b1-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="308b1-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


