---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905770"
---
# <span data-ttu-id="6a073-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="6a073-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="6a073-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a073-102">SYNOPSIS</span></span>
<span data-ttu-id="6a073-103">Восстановление элемента с мягким удалением</span><span class="sxs-lookup"><span data-stu-id="6a073-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="6a073-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a073-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a073-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a073-105">DESCRIPTION</span></span>
<span data-ttu-id="6a073-106">Командлет Undo-AzRecoveryServicesBackupItemDeletion восстановление элемента с мягким удалением.</span><span class="sxs-lookup"><span data-stu-id="6a073-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="6a073-107">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="6a073-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6a073-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a073-108">EXAMPLES</span></span>

### <span data-ttu-id="6a073-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a073-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="6a073-110">Первая команда получает массив контейнеров резервного копирования, а затем сохраняет их в массиве $Cont.</span><span class="sxs-lookup"><span data-stu-id="6a073-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="6a073-111">Вторая команда возвращает элемент резервного копирования, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI.</span><span class="sxs-lookup"><span data-stu-id="6a073-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="6a073-112">Третья команда отключает защиту от резервного копирования для элемента в $PI \[ 0 \] и помещает элемент в состояние softdeleted.</span><span class="sxs-lookup"><span data-stu-id="6a073-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="6a073-113">Четвертая команда нового элемента, который находится в состоянии softdeleted.</span><span class="sxs-lookup"><span data-stu-id="6a073-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="6a073-114">Последняя команда восsoftdeleted ВМ.</span><span class="sxs-lookup"><span data-stu-id="6a073-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="6a073-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a073-115">PARAMETERS</span></span>

### <span data-ttu-id="6a073-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a073-116">-DefaultProfile</span></span>
<span data-ttu-id="6a073-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a073-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a073-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6a073-118">-Force</span></span>
<span data-ttu-id="6a073-119">Force отключить защиту от резервных копий (диалоговое окно подтверждения не задается).</span><span class="sxs-lookup"><span data-stu-id="6a073-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="6a073-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6a073-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a073-121">-Item</span><span class="sxs-lookup"><span data-stu-id="6a073-121">-Item</span></span>
<span data-ttu-id="6a073-122">Указывает элемент резервного копирования, для которого этот командлет отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="6a073-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="6a073-123">Чтобы получить AzureRmRecoveryServicesBackupItem, используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6a073-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="6a073-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6a073-124">-VaultId</span></span>
<span data-ttu-id="6a073-125">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a073-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6a073-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a073-126">-Confirm</span></span>
<span data-ttu-id="6a073-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a073-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a073-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a073-128">-WhatIf</span></span>
<span data-ttu-id="6a073-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a073-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a073-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a073-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a073-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a073-131">CommonParameters</span></span>
<span data-ttu-id="6a073-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a073-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a073-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a073-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a073-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a073-134">INPUTS</span></span>

### <span data-ttu-id="6a073-135">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="6a073-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="6a073-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6a073-136">System.String</span></span>

## <span data-ttu-id="6a073-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a073-137">OUTPUTS</span></span>

### <span data-ttu-id="6a073-138">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6a073-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6a073-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a073-139">NOTES</span></span>

## <span data-ttu-id="6a073-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a073-140">RELATED LINKS</span></span>

[<span data-ttu-id="6a073-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6a073-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="6a073-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6a073-142">Get-AzRecoveryServicesBackupItem</span></span>]()

