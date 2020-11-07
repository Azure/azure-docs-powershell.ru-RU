---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b7e691d3bfea45fc8fc45725ddfe782418c12ab7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914541"
---
# <span data-ttu-id="5397b-101">Remove-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="5397b-101">Remove-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="5397b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5397b-102">SYNOPSIS</span></span>
<span data-ttu-id="5397b-103">Удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="5397b-103">Removes a data disk from an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5397b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5397b-104">SYNTAX</span></span>

```
Remove-AzureRmImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5397b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5397b-105">DESCRIPTION</span></span>
<span data-ttu-id="5397b-106">Командлет **Remove-AzureRmImageDataDisk** удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="5397b-106">The **Remove-AzureRmImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="5397b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5397b-107">EXAMPLES</span></span>

### <span data-ttu-id="5397b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5397b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="5397b-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5397b-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5397b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5397b-110">PARAMETERS</span></span>

### <span data-ttu-id="5397b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5397b-111">-DefaultProfile</span></span>
<span data-ttu-id="5397b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5397b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5397b-113">-Image</span><span class="sxs-lookup"><span data-stu-id="5397b-113">-Image</span></span>
<span data-ttu-id="5397b-114">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="5397b-114">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5397b-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="5397b-115">-Lun</span></span>
<span data-ttu-id="5397b-116">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="5397b-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5397b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5397b-117">-Confirm</span></span>
<span data-ttu-id="5397b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5397b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5397b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5397b-119">-WhatIf</span></span>
<span data-ttu-id="5397b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5397b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5397b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5397b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5397b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5397b-122">CommonParameters</span></span>
<span data-ttu-id="5397b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5397b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5397b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5397b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5397b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5397b-125">INPUTS</span></span>

### <span data-ttu-id="5397b-126">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="5397b-126">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="5397b-127">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5397b-127">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5397b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5397b-128">OUTPUTS</span></span>

### <span data-ttu-id="5397b-129">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="5397b-129">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="5397b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5397b-130">NOTES</span></span>

## <span data-ttu-id="5397b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5397b-131">RELATED LINKS</span></span>

