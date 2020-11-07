---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 49fad6adf339afb9dacd6f916cf0abb8e6bb3728
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902473"
---
# <span data-ttu-id="2d1bc-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d1bc-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="2d1bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1bc-103">Получает массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="2d1bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d1bc-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d1bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="2d1bc-106">Функция **Get-AzAutoApprovedPrivateLinkService** получает массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="2d1bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d1bc-107">EXAMPLES</span></span>

### <span data-ttu-id="2d1bc-108">Образом</span><span class="sxs-lookup"><span data-stu-id="2d1bc-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="2d1bc-109">В этом примере возвращается массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="2d1bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d1bc-110">PARAMETERS</span></span>

### <span data-ttu-id="2d1bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1bc-111">-DefaultProfile</span></span>
<span data-ttu-id="2d1bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1bc-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2d1bc-113">-Location</span></span>
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

### <span data-ttu-id="2d1bc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d1bc-114">-ResourceGroupName</span></span>
<span data-ttu-id="2d1bc-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1bc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1bc-116">CommonParameters</span></span>
<span data-ttu-id="2d1bc-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d1bc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1bc-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d1bc-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1bc-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d1bc-119">INPUTS</span></span>

### <span data-ttu-id="2d1bc-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="2d1bc-120">None</span></span>

## <span data-ttu-id="2d1bc-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d1bc-121">OUTPUTS</span></span>

### <span data-ttu-id="2d1bc-122">Microsoft. Azure. Commands. Network. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d1bc-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="2d1bc-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d1bc-123">NOTES</span></span>

## <span data-ttu-id="2d1bc-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d1bc-124">RELATED LINKS</span></span>
