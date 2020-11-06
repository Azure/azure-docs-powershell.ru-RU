---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7235c70eae1ab7b93340e68bbb705c17b74c3408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558967"
---
# <span data-ttu-id="c70f8-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c70f8-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c70f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c70f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c70f8-103">Отключает защиту для элемента, защищенного резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="c70f8-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c70f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c70f8-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c70f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c70f8-105">DESCRIPTION</span></span>
<span data-ttu-id="c70f8-106">Командлет **Disable-AzureRmRecoveryServicesBackupProtection** отключает защиту для элемента, защищенного резервным копированием Azure.</span><span class="sxs-lookup"><span data-stu-id="c70f8-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="c70f8-107">Этот командлет прекращает обычную архивацию элемента по расписанию.</span><span class="sxs-lookup"><span data-stu-id="c70f8-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="c70f8-108">Этот командлет также может удалить существующие точки восстановления для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="c70f8-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="c70f8-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="c70f8-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c70f8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c70f8-110">EXAMPLES</span></span>

### <span data-ttu-id="c70f8-111">Пример 1: отключение защиты резервного копирования</span><span class="sxs-lookup"><span data-stu-id="c70f8-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="c70f8-112">Первая команда получает массив контейнеров резервного копирования, а затем сохраняет их в массиве $Cont.</span><span class="sxs-lookup"><span data-stu-id="c70f8-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="c70f8-113">Вторая команда возвращает элемент резервного копирования, соответствующий первому элементу контейнера, и сохраняет его в переменной $PI.</span><span class="sxs-lookup"><span data-stu-id="c70f8-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="c70f8-114">Последняя команда отключает защиту от резервного копирования для элемента в $PI \[ 0 \] , но сохраняет данные.</span><span class="sxs-lookup"><span data-stu-id="c70f8-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="c70f8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c70f8-115">PARAMETERS</span></span>

### <span data-ttu-id="c70f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c70f8-116">-DefaultProfile</span></span>
<span data-ttu-id="c70f8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c70f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c70f8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c70f8-118">-Force</span></span>
<span data-ttu-id="c70f8-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c70f8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c70f8-120">-Item</span><span class="sxs-lookup"><span data-stu-id="c70f8-120">-Item</span></span>
<span data-ttu-id="c70f8-121">Указывает элемент резервного копирования, для которого этот командлет отключает защиту.</span><span class="sxs-lookup"><span data-stu-id="c70f8-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="c70f8-122">Чтобы получить **AzureRmRecoveryServicesBackupItem** , используйте командлет Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c70f8-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c70f8-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="c70f8-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="c70f8-124">Указывает на то, что этот командлет удаляет существующие точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="c70f8-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="c70f8-125">Чтобы позднее удалить сохраненные точки восстановления, повторно запустите этот командлет и укажите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c70f8-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c70f8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c70f8-126">-Confirm</span></span>
<span data-ttu-id="c70f8-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c70f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c70f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c70f8-128">-WhatIf</span></span>
<span data-ttu-id="c70f8-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c70f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c70f8-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c70f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c70f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c70f8-131">CommonParameters</span></span>
<span data-ttu-id="c70f8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c70f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c70f8-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c70f8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c70f8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c70f8-134">INPUTS</span></span>

### <span data-ttu-id="c70f8-135">ItemBase</span><span class="sxs-lookup"><span data-stu-id="c70f8-135">ItemBase</span></span>
<span data-ttu-id="c70f8-136">Параметр "элемент" принимает значение типа "ItemBase" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c70f8-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="c70f8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c70f8-137">OUTPUTS</span></span>

### <span data-ttu-id="c70f8-138">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c70f8-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c70f8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c70f8-139">NOTES</span></span>

## <span data-ttu-id="c70f8-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c70f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="c70f8-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c70f8-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c70f8-142">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c70f8-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="c70f8-143">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c70f8-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


