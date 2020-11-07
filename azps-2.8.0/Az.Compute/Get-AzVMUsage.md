---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721888"
---
# <span data-ttu-id="52f12-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="52f12-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="52f12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52f12-102">SYNOPSIS</span></span>
<span data-ttu-id="52f12-103">Возвращает использование счетчика ядра виртуальной машины для местоположения.</span><span class="sxs-lookup"><span data-stu-id="52f12-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="52f12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52f12-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52f12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52f12-105">DESCRIPTION</span></span>
<span data-ttu-id="52f12-106">Командлет **Get-AzVMUsage** получает использование виртуальной машины по количеству ядер для местоположения.</span><span class="sxs-lookup"><span data-stu-id="52f12-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="52f12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52f12-107">EXAMPLES</span></span>

### <span data-ttu-id="52f12-108">Пример 1: получение используемого количества ядер для местоположения</span><span class="sxs-lookup"><span data-stu-id="52f12-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="52f12-109">Эта команда получает использование количества ядер виртуальной машины для централизованного расположения США.</span><span class="sxs-lookup"><span data-stu-id="52f12-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="52f12-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52f12-110">PARAMETERS</span></span>

### <span data-ttu-id="52f12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f12-111">-DefaultProfile</span></span>
<span data-ttu-id="52f12-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52f12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f12-113">-Location</span><span class="sxs-lookup"><span data-stu-id="52f12-113">-Location</span></span>
<span data-ttu-id="52f12-114">Указывает расположение, для которого этот командлет получает использование количества ядер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="52f12-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="52f12-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f12-115">CommonParameters</span></span>
<span data-ttu-id="52f12-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52f12-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f12-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52f12-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f12-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52f12-118">INPUTS</span></span>

### <span data-ttu-id="52f12-119">System. String</span><span class="sxs-lookup"><span data-stu-id="52f12-119">System.String</span></span>

## <span data-ttu-id="52f12-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52f12-120">OUTPUTS</span></span>

### <span data-ttu-id="52f12-121">Microsoft. Azure. Commands. COMPUTE. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="52f12-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="52f12-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="52f12-122">NOTES</span></span>

## <span data-ttu-id="52f12-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52f12-123">RELATED LINKS</span></span>

[<span data-ttu-id="52f12-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="52f12-124">Get-AzVM</span></span>](./Get-AzVM.md)


