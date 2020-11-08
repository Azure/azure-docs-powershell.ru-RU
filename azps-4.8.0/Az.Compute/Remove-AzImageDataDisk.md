---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 20399a1b62062afa5585e78a9fdb229ad3781d33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079116"
---
# <span data-ttu-id="98c07-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="98c07-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="98c07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98c07-102">SYNOPSIS</span></span>
<span data-ttu-id="98c07-103">Удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="98c07-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="98c07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98c07-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c07-105">DESCRIPTION</span></span>
<span data-ttu-id="98c07-106">Командлет **Remove-AzImageDataDisk** удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="98c07-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="98c07-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98c07-107">EXAMPLES</span></span>

### <span data-ttu-id="98c07-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98c07-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="98c07-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="98c07-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="98c07-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98c07-110">PARAMETERS</span></span>

### <span data-ttu-id="98c07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c07-111">-DefaultProfile</span></span>
<span data-ttu-id="98c07-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98c07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c07-113">-Image</span><span class="sxs-lookup"><span data-stu-id="98c07-113">-Image</span></span>
<span data-ttu-id="98c07-114">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="98c07-114">Specifies a local image object.</span></span>

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

### <span data-ttu-id="98c07-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="98c07-115">-Lun</span></span>
<span data-ttu-id="98c07-116">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="98c07-116">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="98c07-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98c07-117">-Confirm</span></span>
<span data-ttu-id="98c07-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98c07-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c07-119">-WhatIf</span></span>
<span data-ttu-id="98c07-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98c07-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c07-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98c07-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c07-122">CommonParameters</span></span>
<span data-ttu-id="98c07-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98c07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c07-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c07-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c07-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98c07-125">INPUTS</span></span>

### <span data-ttu-id="98c07-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="98c07-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="98c07-127">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="98c07-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="98c07-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98c07-128">OUTPUTS</span></span>

### <span data-ttu-id="98c07-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="98c07-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="98c07-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="98c07-130">NOTES</span></span>

## <span data-ttu-id="98c07-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98c07-131">RELATED LINKS</span></span>