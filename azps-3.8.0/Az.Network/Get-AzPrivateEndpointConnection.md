---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073308"
---
# <span data-ttu-id="3ddae-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ddae-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="3ddae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ddae-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddae-103">Получает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="3ddae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ddae-104">SYNTAX</span></span>

### <span data-ttu-id="3ddae-105">ByPrivateLinkResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ddae-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ddae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ddae-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ddae-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="3ddae-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ddae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ddae-108">DESCRIPTION</span></span>
<span data-ttu-id="3ddae-109">Командлет **Get-AzPrivateEndpointConnection** извлекает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="3ddae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ddae-110">EXAMPLES</span></span>

### <span data-ttu-id="3ddae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ddae-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="3ddae-112">В этом примере возвращается список всех частных подключений к конечным точкам, которые относятся к SQL Server с именем MySQL.</span><span class="sxs-lookup"><span data-stu-id="3ddae-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="3ddae-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3ddae-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="3ddae-114">В этом примере показано, как получить подключение к частной конечной точке с именем MyPrivateEndpointConnection1, принадлежащее службе частной ссылки с именем MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3ddae-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="3ddae-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ddae-115">PARAMETERS</span></span>

### <span data-ttu-id="3ddae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddae-116">-DefaultProfile</span></span>
<span data-ttu-id="3ddae-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ddae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ddae-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ddae-118">-Name</span></span>
<span data-ttu-id="3ddae-119">Имя подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-119">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="3ddae-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="3ddae-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="3ddae-121">Идентификатор диспетчера ресурсов Azure для ресурса частной ссылки, к которому относится подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="3ddae-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="3ddae-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="3ddae-123">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="3ddae-123">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ddae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddae-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ddae-125">Имя группы ресурсов для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="3ddae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ddae-126">-ResourceId</span></span>
<span data-ttu-id="3ddae-127">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="3ddae-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3ddae-128">-ServiceName</span></span>
<span data-ttu-id="3ddae-129">Имя службы, к которой принадлежит подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3ddae-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="3ddae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddae-130">CommonParameters</span></span>
<span data-ttu-id="3ddae-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ddae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddae-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ddae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddae-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ddae-133">INPUTS</span></span>

### <span data-ttu-id="3ddae-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddae-134">System.String</span></span>

## <span data-ttu-id="3ddae-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ddae-135">OUTPUTS</span></span>

### <span data-ttu-id="3ddae-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ddae-136">System.Boolean</span></span>

## <span data-ttu-id="3ddae-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ddae-137">NOTES</span></span>

## <span data-ttu-id="3ddae-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ddae-138">RELATED LINKS</span></span>

[<span data-ttu-id="3ddae-139">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ddae-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3ddae-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ddae-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3ddae-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ddae-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3ddae-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3ddae-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
