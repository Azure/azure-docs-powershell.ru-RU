---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317183"
---
# <span data-ttu-id="a284e-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a284e-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a284e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a284e-102">SYNOPSIS</span></span>
<span data-ttu-id="a284e-103">Получает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="a284e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a284e-104">SYNTAX</span></span>

### <span data-ttu-id="a284e-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a284e-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a284e-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a284e-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a284e-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="a284e-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a284e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a284e-108">DESCRIPTION</span></span>
<span data-ttu-id="a284e-109">Командлет **Get-AzPrivateEndpointConnection** извлекает ресурс подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="a284e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a284e-110">EXAMPLES</span></span>

### <span data-ttu-id="a284e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a284e-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="a284e-112">В этом примере возвращается список всех частных подключений к конечным точкам, которые относятся к SQL Server с именем MySQL.</span><span class="sxs-lookup"><span data-stu-id="a284e-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="a284e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a284e-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="a284e-114">В этом примере показано, как получить подключение к частной конечной точке с именем MyPrivateEndpointConnection1, принадлежащее службе частной ссылки с именем MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a284e-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="a284e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a284e-115">PARAMETERS</span></span>

### <span data-ttu-id="a284e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a284e-116">-DefaultProfile</span></span>
<span data-ttu-id="a284e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a284e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a284e-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="a284e-118">-Description</span></span>
<span data-ttu-id="a284e-119">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="a284e-119">The reason of action.</span></span>

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

### <span data-ttu-id="a284e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a284e-120">-Name</span></span>
<span data-ttu-id="a284e-121">Имя подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a284e-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a284e-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a284e-123">Идентификатор диспетчера ресурсов Azure для ресурса частной ссылки, к которому относится подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="a284e-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a284e-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a284e-125">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="a284e-125">The private link resource type.</span></span>

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

### <span data-ttu-id="a284e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a284e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a284e-127">Имя группы ресурсов для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a284e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a284e-128">-ResourceId</span></span>
<span data-ttu-id="a284e-129">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a284e-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a284e-130">-ServiceName</span></span>
<span data-ttu-id="a284e-131">Имя службы, к которой принадлежит подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a284e-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="a284e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a284e-132">CommonParameters</span></span>
<span data-ttu-id="a284e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a284e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a284e-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a284e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a284e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a284e-135">INPUTS</span></span>

### <span data-ttu-id="a284e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a284e-136">System.String</span></span>

## <span data-ttu-id="a284e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a284e-137">OUTPUTS</span></span>

### <span data-ttu-id="a284e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a284e-138">System.Boolean</span></span>

## <span data-ttu-id="a284e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a284e-139">NOTES</span></span>

## <span data-ttu-id="a284e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a284e-140">RELATED LINKS</span></span>

[<span data-ttu-id="a284e-141">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a284e-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a284e-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a284e-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a284e-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a284e-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a284e-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a284e-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
