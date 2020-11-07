---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: 0e3c1a9113bf3872ca86227272e36abd67781b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721904"
---
# <span data-ttu-id="ce0fd-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ce0fd-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="ce0fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0fd-103">Получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="ce0fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce0fd-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce0fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce0fd-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0fd-106">Командлет **Get-AzVMExtensionImageType** получает тип расширения Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="ce0fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce0fd-107">EXAMPLES</span></span>

### <span data-ttu-id="ce0fd-108">Пример 1: получение типа изображения расширения</span><span class="sxs-lookup"><span data-stu-id="ce0fd-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="ce0fd-109">Эта команда получает тип изображения расширения для указанного издателя и места.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="ce0fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce0fd-110">PARAMETERS</span></span>

### <span data-ttu-id="ce0fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0fd-111">-DefaultProfile</span></span>
<span data-ttu-id="ce0fd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce0fd-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ce0fd-113">-Location</span></span>
<span data-ttu-id="ce0fd-114">Указывает расположение расширения.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="ce0fd-115">Этот командлет получает тип расширения в расположении, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0fd-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="ce0fd-116">-PublisherName</span></span>
<span data-ttu-id="ce0fd-117">Указывает имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="ce0fd-118">Чтобы получить издатель расширения, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="ce0fd-119">Этот командлет получает тип расширения от издателя, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0fd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0fd-120">CommonParameters</span></span>
<span data-ttu-id="ce0fd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce0fd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0fd-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce0fd-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0fd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce0fd-123">INPUTS</span></span>

### <span data-ttu-id="ce0fd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0fd-124">System.String</span></span>

## <span data-ttu-id="ce0fd-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce0fd-125">OUTPUTS</span></span>

### <span data-ttu-id="ce0fd-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ce0fd-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="ce0fd-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce0fd-127">NOTES</span></span>

## <span data-ttu-id="ce0fd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce0fd-128">RELATED LINKS</span></span>

[<span data-ttu-id="ce0fd-129">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ce0fd-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="ce0fd-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ce0fd-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


