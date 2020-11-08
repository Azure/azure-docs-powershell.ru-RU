---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245614"
---
# <span data-ttu-id="fa0e1-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="fa0e1-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="fa0e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0e1-103">Возвращает использование счетчика ядра виртуальной машины для местоположения.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="fa0e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa0e1-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa0e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fa0e1-106">Командлет **Get-AzVMUsage** получает использование виртуальной машины по количеству ядер для местоположения.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="fa0e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa0e1-107">EXAMPLES</span></span>

### <span data-ttu-id="fa0e1-108">Пример 1: получение используемого количества ядер для местоположения</span><span class="sxs-lookup"><span data-stu-id="fa0e1-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="fa0e1-109">Эта команда получает использование количества ядер виртуальной машины для централизованного расположения США.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="fa0e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa0e1-110">PARAMETERS</span></span>

### <span data-ttu-id="fa0e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0e1-111">-DefaultProfile</span></span>
<span data-ttu-id="fa0e1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa0e1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="fa0e1-113">-Location</span></span>
<span data-ttu-id="fa0e1-114">Указывает расположение, для которого этот командлет получает использование количества ядер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0e1-115">CommonParameters</span></span>
<span data-ttu-id="fa0e1-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa0e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0e1-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa0e1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0e1-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa0e1-118">INPUTS</span></span>

### <span data-ttu-id="fa0e1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0e1-119">System.String</span></span>

## <span data-ttu-id="fa0e1-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0e1-120">OUTPUTS</span></span>

### <span data-ttu-id="fa0e1-121">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="fa0e1-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="fa0e1-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa0e1-122">NOTES</span></span>

## <span data-ttu-id="fa0e1-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa0e1-123">RELATED LINKS</span></span>

[<span data-ttu-id="fa0e1-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa0e1-124">Get-AzVM</span></span>](./Get-AzVM.md)


