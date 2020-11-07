---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909877"
---
# <span data-ttu-id="93947-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93947-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="93947-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93947-102">SYNOPSIS</span></span>
<span data-ttu-id="93947-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="93947-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="93947-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93947-104">SYNTAX</span></span>

### <span data-ttu-id="93947-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="93947-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93947-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="93947-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93947-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93947-107">DESCRIPTION</span></span>
<span data-ttu-id="93947-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="93947-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="93947-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93947-109">EXAMPLES</span></span>

### <span data-ttu-id="93947-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93947-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="93947-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="93947-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="93947-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93947-112">PARAMETERS</span></span>

### <span data-ttu-id="93947-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93947-113">-DefaultProfile</span></span>
<span data-ttu-id="93947-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93947-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93947-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="93947-115">-ExpandResource</span></span>
<span data-ttu-id="93947-116">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="93947-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93947-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93947-117">-Name</span></span>
<span data-ttu-id="93947-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="93947-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93947-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93947-119">-ResourceGroupName</span></span>
<span data-ttu-id="93947-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93947-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93947-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93947-121">CommonParameters</span></span>
<span data-ttu-id="93947-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93947-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93947-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93947-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93947-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93947-124">INPUTS</span></span>

### <span data-ttu-id="93947-125">System. String</span><span class="sxs-lookup"><span data-stu-id="93947-125">System.String</span></span>

## <span data-ttu-id="93947-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93947-126">OUTPUTS</span></span>

### <span data-ttu-id="93947-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="93947-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="93947-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="93947-128">NOTES</span></span>

## <span data-ttu-id="93947-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93947-129">RELATED LINKS</span></span>

