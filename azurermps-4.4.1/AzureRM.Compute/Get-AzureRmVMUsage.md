---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567145"
---
# <span data-ttu-id="d9ff5-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="d9ff5-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="d9ff5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ff5-103">Возвращает использование счетчика ядра виртуальной машины для местоположения.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9ff5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9ff5-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ff5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ff5-106">Командлет **Get-AzureRmVMUsage** получает использование виртуальной машины по количеству ядер для местоположения.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="d9ff5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9ff5-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ff5-108">Пример 1: получение используемого количества ядер для местоположения</span><span class="sxs-lookup"><span data-stu-id="d9ff5-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="d9ff5-109">Эта команда получает использование количества ядер виртуальной машины для централизованного расположения США.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="d9ff5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9ff5-110">PARAMETERS</span></span>

### <span data-ttu-id="d9ff5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ff5-111">-DefaultProfile</span></span>
<span data-ttu-id="d9ff5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ff5-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d9ff5-113">-Location</span></span>
<span data-ttu-id="d9ff5-114">Указывает расположение, для которого этот командлет получает использование количества ядер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="d9ff5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ff5-115">CommonParameters</span></span>
<span data-ttu-id="d9ff5-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9ff5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ff5-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ff5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ff5-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9ff5-118">INPUTS</span></span>

## <span data-ttu-id="d9ff5-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ff5-119">OUTPUTS</span></span>

## <span data-ttu-id="d9ff5-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9ff5-120">NOTES</span></span>

## <span data-ttu-id="d9ff5-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9ff5-121">RELATED LINKS</span></span>

[<span data-ttu-id="d9ff5-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d9ff5-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


