---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564135"
---
# <span data-ttu-id="03ff1-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="03ff1-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="03ff1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="03ff1-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="03ff1-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03ff1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03ff1-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ff1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="03ff1-106">Командлет Get-AzureRmTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="03ff1-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="03ff1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03ff1-107">EXAMPLES</span></span>

### <span data-ttu-id="03ff1-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="03ff1-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="03ff1-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="03ff1-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="03ff1-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="03ff1-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="03ff1-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="03ff1-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="03ff1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03ff1-112">PARAMETERS</span></span>

### <span data-ttu-id="03ff1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ff1-113">-DefaultProfile</span></span>
<span data-ttu-id="03ff1-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03ff1-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03ff1-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="03ff1-115">-TenantId</span></span>
<span data-ttu-id="03ff1-116">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="03ff1-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03ff1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ff1-117">CommonParameters</span></span>
<span data-ttu-id="03ff1-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03ff1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ff1-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ff1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ff1-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03ff1-120">INPUTS</span></span>

### <span data-ttu-id="03ff1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="03ff1-121">System.String</span></span>

## <span data-ttu-id="03ff1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ff1-122">OUTPUTS</span></span>

### <span data-ttu-id="03ff1-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="03ff1-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="03ff1-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="03ff1-124">NOTES</span></span>

## <span data-ttu-id="03ff1-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03ff1-125">RELATED LINKS</span></span>
