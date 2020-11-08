---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249967"
---
# <span data-ttu-id="55a18-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="55a18-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="55a18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55a18-102">SYNOPSIS</span></span>
<span data-ttu-id="55a18-103">Получает массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="55a18-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="55a18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55a18-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55a18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a18-105">DESCRIPTION</span></span>
<span data-ttu-id="55a18-106">Функция **Get-AzAutoApprovedPrivateLinkService** получает массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="55a18-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="55a18-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55a18-107">EXAMPLES</span></span>

### <span data-ttu-id="55a18-108">Образом</span><span class="sxs-lookup"><span data-stu-id="55a18-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="55a18-109">В этом примере возвращается массив ИД службы частной ссылки, который может быть связан с закрытой конечной точкой с автоматическим утверждением.</span><span class="sxs-lookup"><span data-stu-id="55a18-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="55a18-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55a18-110">PARAMETERS</span></span>

### <span data-ttu-id="55a18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a18-111">-DefaultProfile</span></span>
<span data-ttu-id="55a18-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55a18-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a18-113">-Location</span><span class="sxs-lookup"><span data-stu-id="55a18-113">-Location</span></span>
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

### <span data-ttu-id="55a18-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a18-114">-ResourceGroupName</span></span>
<span data-ttu-id="55a18-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55a18-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="55a18-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a18-116">CommonParameters</span></span>
<span data-ttu-id="55a18-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55a18-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a18-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a18-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a18-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55a18-119">INPUTS</span></span>

### <span data-ttu-id="55a18-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="55a18-120">None</span></span>

## <span data-ttu-id="55a18-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55a18-121">OUTPUTS</span></span>

### <span data-ttu-id="55a18-122">Microsoft. Azure. Commands. Network. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="55a18-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="55a18-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="55a18-123">NOTES</span></span>

## <span data-ttu-id="55a18-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55a18-124">RELATED LINKS</span></span>
