---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558915"
---
# <span data-ttu-id="40b1c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1c-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="40b1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="40b1c-103">Удаление политики защиты резервных копий из хранилища.</span><span class="sxs-lookup"><span data-stu-id="40b1c-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40b1c-104">SYNTAX</span></span>

### <span data-ttu-id="40b1c-105">PolicyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40b1c-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b1c-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="40b1c-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b1c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b1c-107">DESCRIPTION</span></span>
<span data-ttu-id="40b1c-108">Командлет **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** удаляет политики резервного копирования для хранилища.</span><span class="sxs-lookup"><span data-stu-id="40b1c-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="40b1c-109">Прежде чем можно будет удалить политику защиты резервных копий, она не должна содержать ни одного связанного элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="40b1c-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="40b1c-110">Перед удалением политики убедитесь, что все связанные элементы связаны с какой – либо другой политикой.</span><span class="sxs-lookup"><span data-stu-id="40b1c-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="40b1c-111">Чтобы связать другую политику с элементом резервной копии, используйте командлет Enable-AzureRmRecoveryServicesBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="40b1c-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="40b1c-112">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="40b1c-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="40b1c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40b1c-113">EXAMPLES</span></span>

### <span data-ttu-id="40b1c-114">Пример 1: Удаление политики</span><span class="sxs-lookup"><span data-stu-id="40b1c-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="40b1c-115">Первая команда получает политику защиты резервного копирования с именем NewPolicy и сохраняет ее в переменной $Pol.</span><span class="sxs-lookup"><span data-stu-id="40b1c-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="40b1c-116">Вторая команда удаляет объект политики в $Pol.</span><span class="sxs-lookup"><span data-stu-id="40b1c-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="40b1c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40b1c-117">PARAMETERS</span></span>

### <span data-ttu-id="40b1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b1c-118">-DefaultProfile</span></span>
<span data-ttu-id="40b1c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40b1c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b1c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="40b1c-120">-Force</span></span>
<span data-ttu-id="40b1c-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="40b1c-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40b1c-122">-Name</span></span>
<span data-ttu-id="40b1c-123">Задает имя удаляемой политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="40b1c-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40b1c-124">-PassThru</span></span>
<span data-ttu-id="40b1c-125">Возврат политики для удаления.</span><span class="sxs-lookup"><span data-stu-id="40b1c-125">Return the policy to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-126">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="40b1c-126">-Policy</span></span>
<span data-ttu-id="40b1c-127">Задает политику защиты резервного копирования, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="40b1c-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="40b1c-128">Чтобы получить объект **BackupPolicy** , используйте командлет Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="40b1c-128">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b1c-129">-Confirm</span></span>
<span data-ttu-id="40b1c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40b1c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b1c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b1c-131">-WhatIf</span></span>
<span data-ttu-id="40b1c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40b1c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b1c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40b1c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b1c-134">CommonParameters</span></span>
<span data-ttu-id="40b1c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40b1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b1c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b1c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40b1c-137">INPUTS</span></span>

### <span data-ttu-id="40b1c-138">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="40b1c-138">PolicyBase</span></span>
<span data-ttu-id="40b1c-139">Параметр "Policy" принимает значение типа "PolicyBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40b1c-139">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="40b1c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40b1c-140">OUTPUTS</span></span>

## <span data-ttu-id="40b1c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="40b1c-141">NOTES</span></span>

## <span data-ttu-id="40b1c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40b1c-142">RELATED LINKS</span></span>

[<span data-ttu-id="40b1c-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1c-143">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="40b1c-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1c-144">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="40b1c-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="40b1c-145">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


