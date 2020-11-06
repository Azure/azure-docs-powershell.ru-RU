---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557524"
---
# <span data-ttu-id="a6d7e-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="a6d7e-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="a6d7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d7e-103">Задает свойства ссылки на изображение для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6d7e-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6d7e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d7e-106">Командлет **Set-AzureRmSnapshotImageReference** задает свойства ссылок на изображения в объекте snapshot.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="a6d7e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d7e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6d7e-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a6d7e-109">В первой команде создается локальный объект Snapshot с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a6d7e-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a6d7e-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="a6d7e-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a6d7e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a6d7e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6d7e-113">PARAMETERS</span></span>

### <span data-ttu-id="a6d7e-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a6d7e-114">-Id</span></span>
<span data-ttu-id="a6d7e-115">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="a6d7e-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="a6d7e-116">-Lun</span></span>
<span data-ttu-id="a6d7e-117">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="a6d7e-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="a6d7e-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="a6d7e-118">-Snapshot</span></span>
<span data-ttu-id="a6d7e-119">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d7e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6d7e-120">-Confirm</span></span>
<span data-ttu-id="a6d7e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d7e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d7e-122">-WhatIf</span></span>
<span data-ttu-id="a6d7e-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6d7e-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d7e-125">CommonParameters</span></span>
<span data-ttu-id="a6d7e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6d7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d7e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d7e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d7e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6d7e-128">INPUTS</span></span>

### <span data-ttu-id="a6d7e-129">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="a6d7e-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="a6d7e-130">System. String System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a6d7e-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a6d7e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d7e-131">OUTPUTS</span></span>

### <span data-ttu-id="a6d7e-132">Microsoft. Azure. Management. COMPUTE. Models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="a6d7e-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="a6d7e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6d7e-133">NOTES</span></span>

## <span data-ttu-id="a6d7e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6d7e-134">RELATED LINKS</span></span>

