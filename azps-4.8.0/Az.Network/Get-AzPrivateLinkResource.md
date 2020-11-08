---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235023"
---
# <span data-ttu-id="0d487-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0d487-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="0d487-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d487-102">SYNOPSIS</span></span>
<span data-ttu-id="0d487-103">Возвращает ресурс частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="0d487-103">Gets a private link resource.</span></span>

## <span data-ttu-id="0d487-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d487-104">SYNTAX</span></span>

### <span data-ttu-id="0d487-105">ByPrivateLinkResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d487-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d487-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d487-106">DESCRIPTION</span></span>
<span data-ttu-id="0d487-107">Командлет **Get-AzPrivateLinkResource** извлекает все ссылочные ресурсы, принадлежащие PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="0d487-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="0d487-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d487-108">EXAMPLES</span></span>

### <span data-ttu-id="0d487-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d487-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="0d487-110">В этом примере список всех ресурсов частной ссылки nbelong на сервер SQL Server с именем mySql.</span><span class="sxs-lookup"><span data-stu-id="0d487-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="0d487-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d487-111">PARAMETERS</span></span>

### <span data-ttu-id="0d487-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d487-112">-DefaultProfile</span></span>
<span data-ttu-id="0d487-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d487-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d487-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0d487-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0d487-115">Идентификатор диспетчера ресурсов Azure ресурса частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="0d487-115">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="0d487-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d487-116">CommonParameters</span></span>
<span data-ttu-id="0d487-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d487-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d487-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d487-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d487-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d487-119">INPUTS</span></span>

### <span data-ttu-id="0d487-120">System. String</span><span class="sxs-lookup"><span data-stu-id="0d487-120">System.String</span></span>

## <span data-ttu-id="0d487-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d487-121">OUTPUTS</span></span>

### <span data-ttu-id="0d487-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d487-122">System.Boolean</span></span>

## <span data-ttu-id="0d487-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d487-123">NOTES</span></span>

## <span data-ttu-id="0d487-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d487-124">RELATED LINKS</span></span>
