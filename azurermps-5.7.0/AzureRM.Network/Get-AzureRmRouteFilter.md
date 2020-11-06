---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 2c980b981679ddfa3fb2eda473b495f9281c227d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560304"
---
# <span data-ttu-id="32169-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32169-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="32169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32169-102">SYNOPSIS</span></span>
<span data-ttu-id="32169-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="32169-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32169-104">SYNTAX</span></span>

### <span data-ttu-id="32169-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="32169-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32169-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="32169-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32169-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32169-107">DESCRIPTION</span></span>
<span data-ttu-id="32169-108">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="32169-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="32169-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32169-109">EXAMPLES</span></span>

### <span data-ttu-id="32169-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32169-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="32169-111">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="32169-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="32169-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32169-112">PARAMETERS</span></span>

### <span data-ttu-id="32169-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32169-113">-DefaultProfile</span></span>
<span data-ttu-id="32169-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32169-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32169-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="32169-115">-ExpandResource</span></span>
<span data-ttu-id="32169-116">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="32169-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="32169-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32169-117">-Name</span></span>
<span data-ttu-id="32169-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="32169-118">The resource name.</span></span>

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

### <span data-ttu-id="32169-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32169-119">-ResourceGroupName</span></span>
<span data-ttu-id="32169-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32169-120">The resource group name.</span></span>

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

### <span data-ttu-id="32169-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32169-121">CommonParameters</span></span>
<span data-ttu-id="32169-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32169-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32169-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32169-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32169-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32169-124">INPUTS</span></span>

### <span data-ttu-id="32169-125">System. String</span><span class="sxs-lookup"><span data-stu-id="32169-125">System.String</span></span>

## <span data-ttu-id="32169-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32169-126">OUTPUTS</span></span>

### <span data-ttu-id="32169-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="32169-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="32169-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="32169-128">NOTES</span></span>

## <span data-ttu-id="32169-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32169-129">RELATED LINKS</span></span>

