---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 77f01dc2161188660ecdc46086e6c53a29e520f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983299"
---
# <span data-ttu-id="c876b-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="c876b-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="c876b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c876b-102">SYNOPSIS</span></span>
<span data-ttu-id="c876b-103">Удаляет диск данных из объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="c876b-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="c876b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c876b-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c876b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c876b-105">DESCRIPTION</span></span>
<span data-ttu-id="c876b-106">При **этом из объекта-изображения** удаляется диск данных.</span><span class="sxs-lookup"><span data-stu-id="c876b-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="c876b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c876b-107">EXAMPLES</span></span>

### <span data-ttu-id="c876b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c876b-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="c876b-109">Эта команда удаляет диск данных логического блока 1 из существующего изображения "Image01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="c876b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c876b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c876b-110">PARAMETERS</span></span>

### <span data-ttu-id="c876b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c876b-111">-DefaultProfile</span></span>
<span data-ttu-id="c876b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c876b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c876b-113">-Image</span><span class="sxs-lookup"><span data-stu-id="c876b-113">-Image</span></span>
<span data-ttu-id="c876b-114">Определяет объект локального изображения.</span><span class="sxs-lookup"><span data-stu-id="c876b-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c876b-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="c876b-115">-Lun</span></span>
<span data-ttu-id="c876b-116">Определяет логический номер единицы (LUN).</span><span class="sxs-lookup"><span data-stu-id="c876b-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c876b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c876b-117">-Confirm</span></span>
<span data-ttu-id="c876b-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c876b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c876b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c876b-119">-WhatIf</span></span>
<span data-ttu-id="c876b-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c876b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c876b-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c876b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c876b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c876b-122">CommonParameters</span></span>
<span data-ttu-id="c876b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c876b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c876b-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c876b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c876b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c876b-125">INPUTS</span></span>

### <span data-ttu-id="c876b-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="c876b-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="c876b-127">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c876b-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c876b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c876b-128">OUTPUTS</span></span>

### <span data-ttu-id="c876b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="c876b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c876b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c876b-130">NOTES</span></span>

## <span data-ttu-id="c876b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c876b-131">RELATED LINKS</span></span>
