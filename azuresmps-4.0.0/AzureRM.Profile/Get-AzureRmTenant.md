---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555628"
---
# <span data-ttu-id="6ec5f-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="6ec5f-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="6ec5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ec5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec5f-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="6ec5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ec5f-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ec5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ec5f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec5f-106">Командлет Get-AzureRmTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="6ec5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ec5f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ec5f-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="6ec5f-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="6ec5f-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="6ec5f-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="6ec5f-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="6ec5f-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="6ec5f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ec5f-112">PARAMETERS</span></span>

### <span data-ttu-id="6ec5f-113">-TenantId</span><span class="sxs-lookup"><span data-stu-id="6ec5f-113">-TenantId</span></span>
<span data-ttu-id="6ec5f-114">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec5f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec5f-115">CommonParameters</span></span>
<span data-ttu-id="6ec5f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec5f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec5f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec5f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ec5f-118">INPUTS</span></span>

## <span data-ttu-id="6ec5f-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ec5f-119">OUTPUTS</span></span>

### <span data-ttu-id="6ec5f-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="6ec5f-120">PSAzureTenant</span></span>
<span data-ttu-id="6ec5f-121">Этот командлет возвращает ИД клиента и сведения о соответствующем домене для клиентов, которые уполномочены для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6ec5f-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="6ec5f-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ec5f-122">NOTES</span></span>

## <span data-ttu-id="6ec5f-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ec5f-123">RELATED LINKS</span></span>

