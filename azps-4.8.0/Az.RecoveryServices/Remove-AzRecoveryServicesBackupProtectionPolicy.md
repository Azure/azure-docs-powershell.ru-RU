---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234790"
---
# <span data-ttu-id="618ae-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618ae-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="618ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="618ae-102">SYNOPSIS</span></span>
<span data-ttu-id="618ae-103">Удаление политики защиты резервных копий из хранилища.</span><span class="sxs-lookup"><span data-stu-id="618ae-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="618ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="618ae-104">SYNTAX</span></span>

### <span data-ttu-id="618ae-105">PolicyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="618ae-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="618ae-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="618ae-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="618ae-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="618ae-107">DESCRIPTION</span></span>
<span data-ttu-id="618ae-108">Командлет **Remove-AzRecoveryServicesBackupProtectionPolicy** удаляет политики резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="618ae-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="618ae-109">Прежде чем можно будет удалить политику защиты резервных копий, она не должна содержать ни одного связанного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="618ae-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="618ae-110">Перед удалением политики убедитесь, что все связанные элементы связаны с какой – либо другой политикой.</span><span class="sxs-lookup"><span data-stu-id="618ae-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="618ae-111">Чтобы связать другую политику с элементом резервной копии, используйте командлет Enable-AzRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="618ae-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="618ae-112">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="618ae-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="618ae-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="618ae-113">EXAMPLES</span></span>

### <span data-ttu-id="618ae-114">Пример 1: Удаление политики</span><span class="sxs-lookup"><span data-stu-id="618ae-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="618ae-115">Первая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="618ae-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="618ae-116">Вторая команда удаляет объект политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="618ae-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="618ae-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="618ae-117">Example 2</span></span>

<span data-ttu-id="618ae-118">Удаление политики защиты резервных копий из хранилища.</span><span class="sxs-lookup"><span data-stu-id="618ae-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="618ae-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="618ae-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="618ae-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="618ae-120">PARAMETERS</span></span>

### <span data-ttu-id="618ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618ae-121">-DefaultProfile</span></span>
<span data-ttu-id="618ae-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="618ae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618ae-123">-Force</span><span class="sxs-lookup"><span data-stu-id="618ae-123">-Force</span></span>
<span data-ttu-id="618ae-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="618ae-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="618ae-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="618ae-125">-Name</span></span>
<span data-ttu-id="618ae-126">Задает имя удаляемой политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="618ae-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="618ae-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="618ae-127">-PassThru</span></span>
<span data-ttu-id="618ae-128">Возврат политики для удаления.</span><span class="sxs-lookup"><span data-stu-id="618ae-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="618ae-129">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="618ae-129">-Policy</span></span>
<span data-ttu-id="618ae-130">Задает политику защиты резервного копирования, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="618ae-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="618ae-131">Чтобы получить объект **BackupPolicy** , используйте командлет Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="618ae-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="618ae-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="618ae-132">-VaultId</span></span>
<span data-ttu-id="618ae-133">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="618ae-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="618ae-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="618ae-134">-Confirm</span></span>
<span data-ttu-id="618ae-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="618ae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="618ae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618ae-136">-WhatIf</span></span>
<span data-ttu-id="618ae-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="618ae-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="618ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618ae-138">CommonParameters</span></span>
<span data-ttu-id="618ae-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="618ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618ae-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="618ae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618ae-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="618ae-141">INPUTS</span></span>

### <span data-ttu-id="618ae-142">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="618ae-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="618ae-143">System. String</span><span class="sxs-lookup"><span data-stu-id="618ae-143">System.String</span></span>

## <span data-ttu-id="618ae-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="618ae-144">OUTPUTS</span></span>

### <span data-ttu-id="618ae-145">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="618ae-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="618ae-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="618ae-146">NOTES</span></span>

## <span data-ttu-id="618ae-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="618ae-147">RELATED LINKS</span></span>

[<span data-ttu-id="618ae-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618ae-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="618ae-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618ae-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="618ae-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="618ae-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

