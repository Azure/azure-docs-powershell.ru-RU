---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391287"
---
# <span data-ttu-id="151ca-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="151ca-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="151ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="151ca-102">SYNOPSIS</span></span>
<span data-ttu-id="151ca-103">Если элемент резервной копии удален и находится в софт-удалении, эта команда возвращает его в состояние, в котором данные сохраняются навсегда.</span><span class="sxs-lookup"><span data-stu-id="151ca-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="151ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="151ca-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="151ca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="151ca-105">DESCRIPTION</span></span>
<span data-ttu-id="151ca-106">При Undo-AzRecoveryServicesBackupItemDeletion- и обратимый удаленный элемент возвращается к состоянии, когда защита остановлена, но данные сохраняются навсегда.</span><span class="sxs-lookup"><span data-stu-id="151ca-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="151ca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="151ca-107">EXAMPLES</span></span>

### <span data-ttu-id="151ca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="151ca-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="151ca-109">Первая команда получает массив контейнеров резервных копий, а затем сохраняет их в $Cont массиве.</span><span class="sxs-lookup"><span data-stu-id="151ca-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="151ca-110">Вторая команда получает элемент резервной копии, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI контейнера.</span><span class="sxs-lookup"><span data-stu-id="151ca-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="151ca-111">Третья команда отключает защиту от резервного копирования для элемента в $PI 0 и помещает элемент в \[ мягий. \]</span><span class="sxs-lookup"><span data-stu-id="151ca-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="151ca-112">Четвертая команда получает элемент с мягим состоянием.</span><span class="sxs-lookup"><span data-stu-id="151ca-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="151ca-113">Последняя команда обеспечивает слажается до состояния, когда защита останавливается, но данные сохраняются навсегда.</span><span class="sxs-lookup"><span data-stu-id="151ca-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="151ca-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="151ca-114">Example 2</span></span>

<span data-ttu-id="151ca-115">Повлияют на мягкий удаленный элемент.</span><span class="sxs-lookup"><span data-stu-id="151ca-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="151ca-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="151ca-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="151ca-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="151ca-117">PARAMETERS</span></span>

### <span data-ttu-id="151ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="151ca-118">-DefaultProfile</span></span>
<span data-ttu-id="151ca-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="151ca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="151ca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="151ca-120">-Force</span></span>
<span data-ttu-id="151ca-121">Принудительно отключает защиту от резервного копирования (диалоговое окно подтверждения не позволяет).</span><span class="sxs-lookup"><span data-stu-id="151ca-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="151ca-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="151ca-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="151ca-123">-Item</span><span class="sxs-lookup"><span data-stu-id="151ca-123">-Item</span></span>
<span data-ttu-id="151ca-124">Определяет элемент резервной копии, для которого этот cmdlet возвращает удаление.</span><span class="sxs-lookup"><span data-stu-id="151ca-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="151ca-125">Чтобы получить azureRmRecoveryServicesBackupItem, используйте Get-AzRecoveryServicesBackupItem управления.</span><span class="sxs-lookup"><span data-stu-id="151ca-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="151ca-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="151ca-126">-VaultId</span></span>
<span data-ttu-id="151ca-127">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="151ca-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="151ca-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="151ca-128">-Confirm</span></span>
<span data-ttu-id="151ca-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="151ca-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="151ca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="151ca-130">-WhatIf</span></span>
<span data-ttu-id="151ca-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="151ca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="151ca-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="151ca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="151ca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="151ca-133">CommonParameters</span></span>
<span data-ttu-id="151ca-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="151ca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="151ca-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="151ca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="151ca-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="151ca-136">INPUTS</span></span>

### <span data-ttu-id="151ca-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="151ca-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="151ca-138">System.String</span><span class="sxs-lookup"><span data-stu-id="151ca-138">System.String</span></span>

## <span data-ttu-id="151ca-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="151ca-139">OUTPUTS</span></span>

### <span data-ttu-id="151ca-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="151ca-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="151ca-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="151ca-141">NOTES</span></span>

## <span data-ttu-id="151ca-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="151ca-142">RELATED LINKS</span></span>

[<span data-ttu-id="151ca-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="151ca-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="151ca-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="151ca-144">Get-AzRecoveryServicesBackupItem</span></span>]()

