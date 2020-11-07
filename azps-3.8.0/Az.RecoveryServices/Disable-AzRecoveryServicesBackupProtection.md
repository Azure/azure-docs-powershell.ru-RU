---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912790"
---
# <span data-ttu-id="a116d-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a116d-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="a116d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a116d-102">SYNOPSIS</span></span>
<span data-ttu-id="a116d-103">Отключает защиту для элемента, защищенного резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="a116d-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="a116d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a116d-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a116d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a116d-105">DESCRIPTION</span></span>
<span data-ttu-id="a116d-106">Командлет **Disable-AzRecoveryServicesBackupProtection** отключает защиту для элемента, защищенного резервным копированием Azure.</span><span class="sxs-lookup"><span data-stu-id="a116d-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="a116d-107">Этот командлет прекращает обычную архивацию элемента по расписанию.</span><span class="sxs-lookup"><span data-stu-id="a116d-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="a116d-108">Этот командлет также может удалить существующие точки восстановления для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a116d-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="a116d-109">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="a116d-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a116d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a116d-110">EXAMPLES</span></span>

### <span data-ttu-id="a116d-111">Пример 1: отключение защиты резервного копирования</span><span class="sxs-lookup"><span data-stu-id="a116d-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="a116d-112">Первая команда получает массив контейнеров резервного копирования, а затем сохраняет их в массиве $Cont.</span><span class="sxs-lookup"><span data-stu-id="a116d-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="a116d-113">Вторая команда возвращает элемент резервного копирования, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI.</span><span class="sxs-lookup"><span data-stu-id="a116d-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="a116d-114">Последняя команда отключает защиту от резервного копирования для элемента в $PI \[ 0 \] , но сохраняет данные.</span><span class="sxs-lookup"><span data-stu-id="a116d-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="a116d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a116d-115">PARAMETERS</span></span>

### <span data-ttu-id="a116d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a116d-116">-DefaultProfile</span></span>
<span data-ttu-id="a116d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a116d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a116d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a116d-118">-Force</span></span>
<span data-ttu-id="a116d-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a116d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a116d-120">-Item</span><span class="sxs-lookup"><span data-stu-id="a116d-120">-Item</span></span>
<span data-ttu-id="a116d-121">Указывает элемент резервного копирования, для которого этот командлет отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="a116d-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="a116d-122">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="a116d-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="a116d-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="a116d-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="a116d-124">Указывает на то, что этот командлет удаляет существующие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="a116d-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="a116d-125">Чтобы позднее удалить сохраненные точки восстановления, повторно запустите этот командлет и укажите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a116d-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="a116d-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a116d-126">-VaultId</span></span>
<span data-ttu-id="a116d-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a116d-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a116d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a116d-128">-Confirm</span></span>
<span data-ttu-id="a116d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a116d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a116d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a116d-130">-WhatIf</span></span>
<span data-ttu-id="a116d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a116d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a116d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a116d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a116d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a116d-133">CommonParameters</span></span>
<span data-ttu-id="a116d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a116d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a116d-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a116d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a116d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a116d-136">INPUTS</span></span>

### <span data-ttu-id="a116d-137">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="a116d-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="a116d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a116d-138">System.String</span></span>

## <span data-ttu-id="a116d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a116d-139">OUTPUTS</span></span>

### <span data-ttu-id="a116d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a116d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a116d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a116d-141">NOTES</span></span>

## <span data-ttu-id="a116d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a116d-142">RELATED LINKS</span></span>

[<span data-ttu-id="a116d-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a116d-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="a116d-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a116d-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a116d-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a116d-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


