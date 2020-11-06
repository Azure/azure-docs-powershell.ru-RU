---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 8ac36dd86abb996a934b59d064980233c931d214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565183"
---
# <span data-ttu-id="354d8-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="354d8-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="354d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="354d8-102">SYNOPSIS</span></span>
<span data-ttu-id="354d8-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="354d8-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="354d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="354d8-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="354d8-105">DESCRIPTION</span></span>
<span data-ttu-id="354d8-106">Командлет Get-AzureRmTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="354d8-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="354d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="354d8-107">EXAMPLES</span></span>

### <span data-ttu-id="354d8-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="354d8-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="354d8-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="354d8-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="354d8-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="354d8-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="354d8-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="354d8-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="354d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="354d8-112">PARAMETERS</span></span>

### <span data-ttu-id="354d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354d8-113">-DefaultProfile</span></span>
<span data-ttu-id="354d8-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="354d8-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354d8-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="354d8-115">-TenantId</span></span>
<span data-ttu-id="354d8-116">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="354d8-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354d8-117">CommonParameters</span></span>
<span data-ttu-id="354d8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="354d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354d8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354d8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354d8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="354d8-120">INPUTS</span></span>

## <span data-ttu-id="354d8-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="354d8-121">OUTPUTS</span></span>

### <span data-ttu-id="354d8-122">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="354d8-122">PSAzureTenant</span></span>
<span data-ttu-id="354d8-123">Этот командлет возвращает ИД клиента и сведения о соответствующем домене для клиентов, которые уполномочены для текущей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="354d8-123">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="354d8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="354d8-124">NOTES</span></span>

## <span data-ttu-id="354d8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="354d8-125">RELATED LINKS</span></span>

