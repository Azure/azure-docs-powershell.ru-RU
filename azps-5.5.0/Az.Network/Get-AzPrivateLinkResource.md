---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218788"
---
# <span data-ttu-id="46f32-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="46f32-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="46f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f32-102">SYNOPSIS</span></span>
<span data-ttu-id="46f32-103">Получает ресурс закрытой ссылки.</span><span class="sxs-lookup"><span data-stu-id="46f32-103">Gets a private link resource.</span></span>

## <span data-ttu-id="46f32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46f32-104">SYNTAX</span></span>

### <span data-ttu-id="46f32-105">ByPrivateLinkResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46f32-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46f32-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="46f32-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="46f32-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46f32-107">DESCRIPTION</span></span>
<span data-ttu-id="46f32-108">Для получения всех ресурсов связи, принадлежащих PrivateLinkResource, принадлежит ресурс **Get-AzPrivateLinkResource.**</span><span class="sxs-lookup"><span data-stu-id="46f32-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="46f32-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46f32-109">EXAMPLES</span></span>

### <span data-ttu-id="46f32-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46f32-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="46f32-111">В этом примере личные ресурсы ссылки в nbelong —sql server named mySql.</span><span class="sxs-lookup"><span data-stu-id="46f32-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="46f32-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46f32-112">PARAMETERS</span></span>

### <span data-ttu-id="46f32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f32-113">-DefaultProfile</span></span>
<span data-ttu-id="46f32-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46f32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46f32-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="46f32-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="46f32-116">ИД диспетчера ресурсов Azure для ресурса закрытой ссылки.</span><span class="sxs-lookup"><span data-stu-id="46f32-116">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f32-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="46f32-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="46f32-118">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="46f32-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46f32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f32-119">-ResourceGroupName</span></span>
<span data-ttu-id="46f32-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46f32-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f32-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46f32-121">-ServiceName</span></span>
<span data-ttu-id="46f32-122">Имя службы личной ссылки.</span><span class="sxs-lookup"><span data-stu-id="46f32-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46f32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f32-123">CommonParameters</span></span>
<span data-ttu-id="46f32-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f32-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46f32-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f32-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46f32-126">INPUTS</span></span>

### <span data-ttu-id="46f32-127">System.String</span><span class="sxs-lookup"><span data-stu-id="46f32-127">System.String</span></span>

## <span data-ttu-id="46f32-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46f32-128">OUTPUTS</span></span>

### <span data-ttu-id="46f32-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46f32-129">System.Boolean</span></span>

## <span data-ttu-id="46f32-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46f32-130">NOTES</span></span>

## <span data-ttu-id="46f32-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46f32-131">RELATED LINKS</span></span>
