---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c66eda488b0b7876317b02db279202a88bbcc3d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565940"
---
# <span data-ttu-id="6f742-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6f742-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="6f742-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f742-102">SYNOPSIS</span></span>
<span data-ttu-id="6f742-103">Связывает элемент с политикой защиты резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="6f742-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f742-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f742-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f742-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f742-105">DESCRIPTION</span></span>
<span data-ttu-id="6f742-106">Командлет **Enable-AzureRmBackupProtection** связывает элемент с политикой защиты резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="6f742-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="6f742-107">Чтобы включить политику защиты, необходимо сначала создать существующий элемент резервной копии и существующую политику.</span><span class="sxs-lookup"><span data-stu-id="6f742-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="6f742-108">Оба должны принадлежать одному хранилищу резервных копий.</span><span class="sxs-lookup"><span data-stu-id="6f742-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="6f742-109">Расписание резервного копирования производит полную начальную копию элемента и добавочную копию для последующих резервных копий.</span><span class="sxs-lookup"><span data-stu-id="6f742-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="6f742-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f742-110">EXAMPLES</span></span>

### <span data-ttu-id="6f742-111">Пример 1: Включение защиты на виртуальной машине Azure</span><span class="sxs-lookup"><span data-stu-id="6f742-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="6f742-112">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="6f742-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="6f742-113">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="6f742-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="6f742-114">Вторая команда получает политику защиты резервного копирования с именем DefaultPolicy для хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="6f742-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="6f742-115">Команда сохраняет этот объект в переменной $Policy.</span><span class="sxs-lookup"><span data-stu-id="6f742-115">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="6f742-116">В последней команде для передачи значений из одного командлета в другой используется оператор конвейера.</span><span class="sxs-lookup"><span data-stu-id="6f742-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="6f742-117">Он получает контейнер с помощью командлета Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="6f742-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="6f742-118">Команда получает элемент резервного копирования из этого контейнера с помощью командлета Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6f742-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="6f742-119">Текущий командлет включает политику, хранящуюся в $Policy для элемента, который команда передает этому командлету.</span><span class="sxs-lookup"><span data-stu-id="6f742-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="6f742-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f742-120">PARAMETERS</span></span>

### <span data-ttu-id="6f742-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f742-121">-DefaultProfile</span></span>
<span data-ttu-id="6f742-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f742-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f742-123">-Item</span><span class="sxs-lookup"><span data-stu-id="6f742-123">-Item</span></span>
<span data-ttu-id="6f742-124">Указывает элемент резервного копирования, для которого этот командлет включит защиту.</span><span class="sxs-lookup"><span data-stu-id="6f742-124">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="6f742-125">Чтобы получить **AzureRmBackupItem** , используйте командлет Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="6f742-125">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f742-126">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="6f742-126">-Policy</span></span>
<span data-ttu-id="6f742-127">Задает политику защиты, которую этот командлет связывает с элементом.</span><span class="sxs-lookup"><span data-stu-id="6f742-127">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="6f742-128">Чтобы получить объект **AzureRmBackupProtectionPolicy** , используйте командлет Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="6f742-128">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f742-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f742-129">CommonParameters</span></span>
<span data-ttu-id="6f742-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f742-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f742-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f742-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f742-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f742-132">INPUTS</span></span>

### <span data-ttu-id="6f742-133">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainerContextObject</span><span class="sxs-lookup"><span data-stu-id="6f742-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject</span></span>
<span data-ttu-id="6f742-134">Параметры: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f742-134">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="6f742-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f742-135">OUTPUTS</span></span>

### <span data-ttu-id="6f742-136">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="6f742-136">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="6f742-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f742-137">NOTES</span></span>

## <span data-ttu-id="6f742-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f742-138">RELATED LINKS</span></span>

[<span data-ttu-id="6f742-139">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="6f742-139">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="6f742-140">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="6f742-140">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="6f742-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f742-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


