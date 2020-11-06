---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565585"
---
# <span data-ttu-id="610ef-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="610ef-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="610ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="610ef-102">SYNOPSIS</span></span>
<span data-ttu-id="610ef-103">Возвращает точки восстановления для резервного элемента.</span><span class="sxs-lookup"><span data-stu-id="610ef-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="610ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="610ef-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="610ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="610ef-105">DESCRIPTION</span></span>
<span data-ttu-id="610ef-106">Командлет **Get-AzureRmBackupRecoveryPoint** получает точки восстановления для резервной копии элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="610ef-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="610ef-107">После создания резервной копии элемента резервная копия хранит одну или несколько точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="610ef-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="610ef-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="610ef-108">EXAMPLES</span></span>

### <span data-ttu-id="610ef-109">Пример 1: получение точек восстановления для элемента</span><span class="sxs-lookup"><span data-stu-id="610ef-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="610ef-110">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="610ef-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="610ef-111">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="610ef-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="610ef-112">Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="610ef-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="610ef-113">Команда сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="610ef-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="610ef-114">Третья команда возвращает элемент резервного копирования в контейнере $Container с помощью командлета **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="610ef-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="610ef-115">Команда сохраняет этот объект в переменной $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="610ef-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="610ef-116">Последняя команда получает точки восстановления для элемента в $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="610ef-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="610ef-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="610ef-117">PARAMETERS</span></span>

### <span data-ttu-id="610ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610ef-118">-DefaultProfile</span></span>
<span data-ttu-id="610ef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="610ef-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="610ef-120">-Item</span><span class="sxs-lookup"><span data-stu-id="610ef-120">-Item</span></span>
<span data-ttu-id="610ef-121">Указывает элемент, для которого этот командлет получает точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="610ef-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="610ef-122">Чтобы получить **AzureRmBackupItem** , используйте командлет Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="610ef-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="610ef-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="610ef-123">-RecoveryPointId</span></span>
<span data-ttu-id="610ef-124">Указывает идентификатор точки восстановления, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="610ef-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610ef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610ef-125">CommonParameters</span></span>
<span data-ttu-id="610ef-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="610ef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610ef-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="610ef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610ef-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="610ef-128">INPUTS</span></span>

### <span data-ttu-id="610ef-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="610ef-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="610ef-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="610ef-130">OUTPUTS</span></span>

### <span data-ttu-id="610ef-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="610ef-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="610ef-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="610ef-132">NOTES</span></span>

## <span data-ttu-id="610ef-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="610ef-133">RELATED LINKS</span></span>

[<span data-ttu-id="610ef-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="610ef-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="610ef-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="610ef-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="610ef-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="610ef-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


