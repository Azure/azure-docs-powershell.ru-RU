---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911504"
---
# <span data-ttu-id="8ece6-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="8ece6-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="8ece6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ece6-102">SYNOPSIS</span></span>
<span data-ttu-id="8ece6-103">Возвращает использование счетчика ядра виртуальной машины для местоположения.</span><span class="sxs-lookup"><span data-stu-id="8ece6-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="8ece6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ece6-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ece6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ece6-105">DESCRIPTION</span></span>
<span data-ttu-id="8ece6-106">Командлет **Get-AzVMUsage** получает использование виртуальной машины по количеству ядер для местоположения.</span><span class="sxs-lookup"><span data-stu-id="8ece6-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="8ece6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ece6-107">EXAMPLES</span></span>

### <span data-ttu-id="8ece6-108">Пример 1: получение используемого количества ядер для местоположения</span><span class="sxs-lookup"><span data-stu-id="8ece6-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="8ece6-109">Эта команда получает использование количества ядер виртуальной машины для централизованного расположения США.</span><span class="sxs-lookup"><span data-stu-id="8ece6-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="8ece6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ece6-110">PARAMETERS</span></span>

### <span data-ttu-id="8ece6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ece6-111">-DefaultProfile</span></span>
<span data-ttu-id="8ece6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ece6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ece6-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8ece6-113">-Location</span></span>
<span data-ttu-id="8ece6-114">Указывает расположение, для которого этот командлет получает использование количества ядер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8ece6-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="8ece6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ece6-115">CommonParameters</span></span>
<span data-ttu-id="8ece6-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ece6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ece6-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ece6-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ece6-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ece6-118">INPUTS</span></span>

### <span data-ttu-id="8ece6-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="8ece6-119">None</span></span>
<span data-ttu-id="8ece6-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8ece6-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ece6-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ece6-121">OUTPUTS</span></span>

### <span data-ttu-id="8ece6-122">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="8ece6-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="8ece6-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ece6-123">NOTES</span></span>

## <span data-ttu-id="8ece6-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ece6-124">RELATED LINKS</span></span>

[<span data-ttu-id="8ece6-125">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ece6-125">Get-AzVM</span></span>](./Get-AzVM.md)


