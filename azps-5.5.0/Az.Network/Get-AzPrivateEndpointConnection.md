---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218796"
---
# <span data-ttu-id="2e057-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e057-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="2e057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e057-102">SYNOPSIS</span></span>
<span data-ttu-id="2e057-103">Возвращает ресурс подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="2e057-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e057-104">SYNTAX</span></span>

### <span data-ttu-id="2e057-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e057-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e057-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="2e057-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e057-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="2e057-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e057-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e057-108">DESCRIPTION</span></span>
<span data-ttu-id="2e057-109">Для получения ресурса подключения к закрытой конечной точке извлекется cmdlet **Get-AzPrivateEndpointConnection.**</span><span class="sxs-lookup"><span data-stu-id="2e057-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="2e057-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e057-110">EXAMPLES</span></span>

### <span data-ttu-id="2e057-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e057-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="2e057-112">В этом примере возвращается список всех подключений частных конечных точек, принадлежащих SQL-серверу Mysql.</span><span class="sxs-lookup"><span data-stu-id="2e057-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="2e057-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2e057-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="2e057-114">В этом примере частное подключение конечной точки с именем MyPrivateEndpointConnection1 принадлежит к службе личной ссылки MyPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="2e057-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="2e057-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e057-115">PARAMETERS</span></span>

### <span data-ttu-id="2e057-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e057-116">-DefaultProfile</span></span>
<span data-ttu-id="2e057-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e057-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e057-118">-Description</span><span class="sxs-lookup"><span data-stu-id="2e057-118">-Description</span></span>
<span data-ttu-id="2e057-119">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="2e057-119">The reason of action.</span></span>

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

### <span data-ttu-id="2e057-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2e057-120">-Name</span></span>
<span data-ttu-id="2e057-121">Имя подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-121">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e057-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="2e057-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="2e057-123">Ид диспетчера ресурсов Azure для ресурса закрытой ссылки, к которой относится подключение к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="2e057-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="2e057-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="2e057-125">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="2e057-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e057-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e057-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e057-127">Имя группы ресурсов подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="2e057-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e057-128">-ResourceId</span></span>
<span data-ttu-id="2e057-129">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e057-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e057-130">-ServiceName</span></span>
<span data-ttu-id="2e057-131">Имя службы, к которую относится частное подключение к конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2e057-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="2e057-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e057-132">CommonParameters</span></span>
<span data-ttu-id="2e057-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e057-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e057-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e057-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e057-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e057-135">INPUTS</span></span>

### <span data-ttu-id="2e057-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e057-136">System.String</span></span>

## <span data-ttu-id="2e057-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e057-137">OUTPUTS</span></span>

### <span data-ttu-id="2e057-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e057-138">System.Boolean</span></span>

## <span data-ttu-id="2e057-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e057-139">NOTES</span></span>

## <span data-ttu-id="2e057-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e057-140">RELATED LINKS</span></span>

[<span data-ttu-id="2e057-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e057-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e057-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e057-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e057-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e057-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="2e057-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2e057-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
