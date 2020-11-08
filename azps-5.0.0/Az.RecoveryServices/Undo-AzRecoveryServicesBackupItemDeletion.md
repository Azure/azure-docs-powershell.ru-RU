---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246845"
---
# <span data-ttu-id="41b04-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="41b04-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="41b04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41b04-102">SYNOPSIS</span></span>
<span data-ttu-id="41b04-103">Если элемент резервного копирования удален и находится в состоянии с мягким удалением, эта команда возвращает элемент в состояние, в котором данные хранятся непостоянно.</span><span class="sxs-lookup"><span data-stu-id="41b04-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="41b04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41b04-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b04-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41b04-105">DESCRIPTION</span></span>
<span data-ttu-id="41b04-106">Командлет Undo-AzRecoveryServicesBackupItemDeletion Возвращает элемент с мягким удалением в состояние, в котором защита остановлена, но данные сохраняются бессрочно.</span><span class="sxs-lookup"><span data-stu-id="41b04-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="41b04-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41b04-107">EXAMPLES</span></span>

### <span data-ttu-id="41b04-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41b04-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="41b04-109">Первая команда получает массив контейнеров резервного копирования, а затем сохраняет их в массиве $Cont.</span><span class="sxs-lookup"><span data-stu-id="41b04-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="41b04-110">Вторая команда возвращает элемент резервного копирования, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI.</span><span class="sxs-lookup"><span data-stu-id="41b04-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="41b04-111">Третья команда отключает защиту от резервного копирования для элемента в $PI \[ 0 \] и помещает элемент в состояние softdeleted.</span><span class="sxs-lookup"><span data-stu-id="41b04-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="41b04-112">Четвертая команда возвращает элемент, который находится в состоянии softdeleted.</span><span class="sxs-lookup"><span data-stu-id="41b04-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="41b04-113">Последняя команда переводит виртуальную машину softdeleted в состояние, в котором она останавливается, но данные сохраняются постоянно.</span><span class="sxs-lookup"><span data-stu-id="41b04-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="41b04-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41b04-114">Example 2</span></span>

<span data-ttu-id="41b04-115">Восстановление элемента с мягким удалением.</span><span class="sxs-lookup"><span data-stu-id="41b04-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="41b04-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="41b04-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="41b04-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41b04-117">PARAMETERS</span></span>

### <span data-ttu-id="41b04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b04-118">-DefaultProfile</span></span>
<span data-ttu-id="41b04-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41b04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b04-120">-Force</span><span class="sxs-lookup"><span data-stu-id="41b04-120">-Force</span></span>
<span data-ttu-id="41b04-121">Force отключить защиту от резервных копий (диалоговое окно подтверждения не задается).</span><span class="sxs-lookup"><span data-stu-id="41b04-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="41b04-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="41b04-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="41b04-123">-Item</span><span class="sxs-lookup"><span data-stu-id="41b04-123">-Item</span></span>
<span data-ttu-id="41b04-124">Указывает элемент резервного копирования, для которого этот командлет отменит удаление.</span><span class="sxs-lookup"><span data-stu-id="41b04-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="41b04-125">Чтобы получить AzureRmRecoveryServicesBackupItem, используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="41b04-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="41b04-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="41b04-126">-VaultId</span></span>
<span data-ttu-id="41b04-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="41b04-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="41b04-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41b04-128">-Confirm</span></span>
<span data-ttu-id="41b04-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41b04-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b04-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b04-130">-WhatIf</span></span>
<span data-ttu-id="41b04-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41b04-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b04-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41b04-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b04-133">CommonParameters</span></span>
<span data-ttu-id="41b04-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41b04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b04-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41b04-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b04-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41b04-136">INPUTS</span></span>

### <span data-ttu-id="41b04-137">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="41b04-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="41b04-138">System. String</span><span class="sxs-lookup"><span data-stu-id="41b04-138">System.String</span></span>

## <span data-ttu-id="41b04-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41b04-139">OUTPUTS</span></span>

### <span data-ttu-id="41b04-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="41b04-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="41b04-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="41b04-141">NOTES</span></span>

## <span data-ttu-id="41b04-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41b04-142">RELATED LINKS</span></span>

[<span data-ttu-id="41b04-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="41b04-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="41b04-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="41b04-144">Get-AzRecoveryServicesBackupItem</span></span>]()

