---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395884"
---
# <span data-ttu-id="ba62e-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="ba62e-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="ba62e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba62e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba62e-103">Задает свойства ссылки на изображение на диске.</span><span class="sxs-lookup"><span data-stu-id="ba62e-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="ba62e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba62e-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba62e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba62e-105">DESCRIPTION</span></span>
<span data-ttu-id="ba62e-106">Cmdlet **Set-AzDiskImageReference** задает свойства ссылки на изображение на объекте диска.</span><span class="sxs-lookup"><span data-stu-id="ba62e-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="ba62e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba62e-107">EXAMPLES</span></span>

### <span data-ttu-id="ba62e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba62e-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ba62e-109">Первая команда создает объект локального диска размером 10 ГБ в Premium_LRS учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ba62e-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ba62e-110">Она также задает тип ОС Windows.</span><span class="sxs-lookup"><span data-stu-id="ba62e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ba62e-111">Вторая команда задает для объекта диска номер изображения и логическую единицу 0.</span><span class="sxs-lookup"><span data-stu-id="ba62e-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="ba62e-112">Последняя команда принимает объект диска и создает диск с именем "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="ba62e-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ba62e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba62e-113">PARAMETERS</span></span>

### <span data-ttu-id="ba62e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba62e-114">-DefaultProfile</span></span>
<span data-ttu-id="ba62e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba62e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba62e-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="ba62e-116">-Disk</span></span>
<span data-ttu-id="ba62e-117">Определяет объект локального диска.</span><span class="sxs-lookup"><span data-stu-id="ba62e-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba62e-118">-Id</span><span class="sxs-lookup"><span data-stu-id="ba62e-118">-Id</span></span>
<span data-ttu-id="ba62e-119">Определяет ИД.</span><span class="sxs-lookup"><span data-stu-id="ba62e-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba62e-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="ba62e-120">-Lun</span></span>
<span data-ttu-id="ba62e-121">Определяет логический номер единицы (LUN).</span><span class="sxs-lookup"><span data-stu-id="ba62e-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba62e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba62e-122">-Confirm</span></span>
<span data-ttu-id="ba62e-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba62e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba62e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba62e-124">-WhatIf</span></span>
<span data-ttu-id="ba62e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba62e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba62e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ba62e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba62e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba62e-127">CommonParameters</span></span>
<span data-ttu-id="ba62e-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba62e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba62e-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba62e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba62e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba62e-130">INPUTS</span></span>

### <span data-ttu-id="ba62e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="ba62e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="ba62e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ba62e-132">System.String</span></span>

### <span data-ttu-id="ba62e-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ba62e-133">System.Int32</span></span>

## <span data-ttu-id="ba62e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba62e-134">OUTPUTS</span></span>

### <span data-ttu-id="ba62e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="ba62e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ba62e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba62e-136">NOTES</span></span>

## <span data-ttu-id="ba62e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba62e-137">RELATED LINKS</span></span>
