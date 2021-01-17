---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 9dc42a137d3abcd23a64e096117be8d287571ecf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398831"
---
# <span data-ttu-id="9ac0e-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9ac0e-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9ac0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac0e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac0e-103">Отключает защиту элемента, защищенного резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="9ac0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ac0e-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ac0e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ac0e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac0e-106">**Cmdlet Disable-AzRecoveryServicesBackupProtection** отключает защиту для элемента, защищенного резервным копированием Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="9ac0e-107">Этот cmdlet останавливает обычное запланированное резервное копирование элемента.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="9ac0e-108">Этот cmdlet также может удалить существующие точки восстановления для элемента резервной копии, если он выполнен с параметром RemoveRecoveryPoints.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-108">This cmdlet can also delete existing recovery points for the backup item if executed with RemoveRecoveryPoints parameter.</span></span>
<span data-ttu-id="9ac0e-109">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9ac0e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ac0e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ac0e-111">Пример 1. Отключение защиты от резервного копирования</span><span class="sxs-lookup"><span data-stu-id="9ac0e-111">Example 1: Disable Backup protection</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="9ac0e-112">Первая команда получает массив контейнеров резервных копий, а затем сохраняет их в $Cont массиве.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="9ac0e-113">Вторая команда получает элемент резервной копии, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI контейнера.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="9ac0e-114">Последняя команда отключает защиту резервного копирования для элемента $PI \[ 0, но \] сохраняет данные.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

### <span data-ttu-id="9ac0e-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9ac0e-115">Example 2</span></span>

<span data-ttu-id="9ac0e-116">Отключает защиту элемента, защищенного резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-116">Disables protection for a Backup-protected item.</span></span> <span data-ttu-id="9ac0e-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="9ac0e-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints -VaultId $vault.ID
```

## <span data-ttu-id="9ac0e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ac0e-118">PARAMETERS</span></span>

### <span data-ttu-id="9ac0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac0e-119">-DefaultProfile</span></span>
<span data-ttu-id="9ac0e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac0e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9ac0e-121">-Force</span></span>
<span data-ttu-id="9ac0e-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ac0e-123">-Item</span><span class="sxs-lookup"><span data-stu-id="9ac0e-123">-Item</span></span>
<span data-ttu-id="9ac0e-124">Элемент резервной копии, для которого этот cmdlet отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-124">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="9ac0e-125">Чтобы получить **azureRmRecoveryServicesBackupItem,** используйте Get-AzRecoveryServicesBackupItem управления.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-125">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac0e-126">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="9ac0e-126">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="9ac0e-127">Указывает на то, что этот cmdlet удаляет существующие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-127">Indicates that this cmdlet deletes existing recovery points.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac0e-128">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9ac0e-128">-VaultId</span></span>
<span data-ttu-id="9ac0e-129">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-129">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9ac0e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ac0e-130">-Confirm</span></span>
<span data-ttu-id="9ac0e-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ac0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ac0e-132">-WhatIf</span></span>
<span data-ttu-id="9ac0e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ac0e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ac0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac0e-135">CommonParameters</span></span>
<span data-ttu-id="9ac0e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac0e-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ac0e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac0e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ac0e-138">INPUTS</span></span>

### <span data-ttu-id="9ac0e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="9ac0e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="9ac0e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9ac0e-140">System.String</span></span>

## <span data-ttu-id="9ac0e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ac0e-141">OUTPUTS</span></span>

### <span data-ttu-id="9ac0e-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="9ac0e-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9ac0e-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ac0e-143">NOTES</span></span>

## <span data-ttu-id="9ac0e-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ac0e-144">RELATED LINKS</span></span>

[<span data-ttu-id="9ac0e-145">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9ac0e-145">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9ac0e-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9ac0e-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9ac0e-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9ac0e-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


