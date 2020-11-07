---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915394"
---
# <span data-ttu-id="3f178-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="3f178-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="3f178-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f178-102">SYNOPSIS</span></span>
<span data-ttu-id="3f178-103">Возвращает использование счетчика ядра виртуальной машины для местоположения.</span><span class="sxs-lookup"><span data-stu-id="3f178-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f178-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f178-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f178-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f178-105">DESCRIPTION</span></span>
<span data-ttu-id="3f178-106">Командлет **Get-AzureRmVMUsage** получает использование виртуальной машины по количеству ядер для местоположения.</span><span class="sxs-lookup"><span data-stu-id="3f178-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="3f178-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f178-107">EXAMPLES</span></span>

### <span data-ttu-id="3f178-108">Пример 1: получение используемого количества ядер для местоположения</span><span class="sxs-lookup"><span data-stu-id="3f178-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="3f178-109">Эта команда получает использование количества ядер виртуальной машины для централизованного расположения США.</span><span class="sxs-lookup"><span data-stu-id="3f178-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="3f178-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f178-110">PARAMETERS</span></span>

### <span data-ttu-id="3f178-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f178-111">-DefaultProfile</span></span>
<span data-ttu-id="3f178-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f178-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f178-113">-Location</span><span class="sxs-lookup"><span data-stu-id="3f178-113">-Location</span></span>
<span data-ttu-id="3f178-114">Указывает расположение, для которого этот командлет получает использование количества ядер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3f178-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f178-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f178-115">CommonParameters</span></span>
<span data-ttu-id="3f178-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f178-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f178-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f178-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f178-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f178-118">INPUTS</span></span>

### <span data-ttu-id="3f178-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="3f178-119">None</span></span>
<span data-ttu-id="3f178-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3f178-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f178-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f178-121">OUTPUTS</span></span>

### <span data-ttu-id="3f178-122">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="3f178-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="3f178-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f178-123">NOTES</span></span>

## <span data-ttu-id="3f178-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f178-124">RELATED LINKS</span></span>

[<span data-ttu-id="3f178-125">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3f178-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


