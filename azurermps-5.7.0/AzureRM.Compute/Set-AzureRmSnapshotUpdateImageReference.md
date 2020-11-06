---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559160"
---
# <span data-ttu-id="32e2b-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="32e2b-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="32e2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="32e2b-103">Задает свойства ссылки на изображение для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="32e2b-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32e2b-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="32e2b-106">Командлет **Set-AzureRmSnapshotUpdateImageReference** задает свойства ссылок на изображения в объекте обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="32e2b-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="32e2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32e2b-107">EXAMPLES</span></span>

### <span data-ttu-id="32e2b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32e2b-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="32e2b-109">Первая команда создает локальный объект обновления моментальных снимков размером 10 ГБ в Premium_LRS тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="32e2b-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="32e2b-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="32e2b-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="32e2b-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="32e2b-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="32e2b-112">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="32e2b-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="32e2b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32e2b-113">PARAMETERS</span></span>

### <span data-ttu-id="32e2b-114">-ID</span><span class="sxs-lookup"><span data-stu-id="32e2b-114">-Id</span></span>
<span data-ttu-id="32e2b-115">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="32e2b-115">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e2b-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="32e2b-116">-Lun</span></span>
<span data-ttu-id="32e2b-117">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="32e2b-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32e2b-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="32e2b-118">-SnapshotUpdate</span></span>
<span data-ttu-id="32e2b-119">Указывает локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="32e2b-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32e2b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32e2b-120">-Confirm</span></span>
<span data-ttu-id="32e2b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32e2b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e2b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e2b-122">-WhatIf</span></span>
<span data-ttu-id="32e2b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32e2b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32e2b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32e2b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e2b-125">CommonParameters</span></span>
<span data-ttu-id="32e2b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32e2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e2b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e2b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e2b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32e2b-128">INPUTS</span></span>

### <span data-ttu-id="32e2b-129">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="32e2b-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="32e2b-130">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="32e2b-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="32e2b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32e2b-131">OUTPUTS</span></span>

### <span data-ttu-id="32e2b-132">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="32e2b-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="32e2b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="32e2b-133">NOTES</span></span>

## <span data-ttu-id="32e2b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32e2b-134">RELATED LINKS</span></span>

