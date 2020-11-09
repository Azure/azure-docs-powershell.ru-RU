---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317180"
---
# <span data-ttu-id="f17c8-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f17c8-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="f17c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f17c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f17c8-103">Возвращает ресурс частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="f17c8-103">Gets a private link resource.</span></span>

## <span data-ttu-id="f17c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f17c8-104">SYNTAX</span></span>

### <span data-ttu-id="f17c8-105">ByPrivateLinkResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f17c8-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f17c8-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="f17c8-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="f17c8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f17c8-107">DESCRIPTION</span></span>
<span data-ttu-id="f17c8-108">Командлет **Get-AzPrivateLinkResource** извлекает все ссылочные ресурсы, принадлежащие PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="f17c8-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="f17c8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f17c8-109">EXAMPLES</span></span>

### <span data-ttu-id="f17c8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f17c8-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="f17c8-111">В этом примере список всех ресурсов частной ссылки nbelong на сервер SQL Server с именем mySql.</span><span class="sxs-lookup"><span data-stu-id="f17c8-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="f17c8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f17c8-112">PARAMETERS</span></span>

### <span data-ttu-id="f17c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17c8-113">-DefaultProfile</span></span>
<span data-ttu-id="f17c8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f17c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f17c8-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f17c8-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f17c8-116">Идентификатор диспетчера ресурсов Azure ресурса частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="f17c8-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="f17c8-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="f17c8-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="f17c8-118">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="f17c8-118">The private link resource type.</span></span>

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

### <span data-ttu-id="f17c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f17c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="f17c8-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f17c8-120">The resource group name.</span></span>

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

### <span data-ttu-id="f17c8-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f17c8-121">-ServiceName</span></span>
<span data-ttu-id="f17c8-122">Имя службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="f17c8-122">The private link service name.</span></span>

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

### <span data-ttu-id="f17c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17c8-123">CommonParameters</span></span>
<span data-ttu-id="f17c8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f17c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17c8-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f17c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17c8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f17c8-126">INPUTS</span></span>

### <span data-ttu-id="f17c8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f17c8-127">System.String</span></span>

## <span data-ttu-id="f17c8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f17c8-128">OUTPUTS</span></span>

### <span data-ttu-id="f17c8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f17c8-129">System.Boolean</span></span>

## <span data-ttu-id="f17c8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f17c8-130">NOTES</span></span>

## <span data-ttu-id="f17c8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f17c8-131">RELATED LINKS</span></span>
