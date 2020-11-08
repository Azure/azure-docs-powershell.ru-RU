---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243419"
---
# <span data-ttu-id="a2bc8-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="a2bc8-101">Get-AzTenant</span></span>

## <span data-ttu-id="a2bc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bc8-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="a2bc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2bc8-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2bc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="a2bc8-106">Командлет Get-AzTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="a2bc8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="a2bc8-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="a2bc8-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="a2bc8-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="a2bc8-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="a2bc8-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="a2bc8-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="a2bc8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2bc8-112">PARAMETERS</span></span>

### <span data-ttu-id="a2bc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bc8-113">-DefaultProfile</span></span>
<span data-ttu-id="a2bc8-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2bc8-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2bc8-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="a2bc8-115">-TenantId</span></span>
<span data-ttu-id="a2bc8-116">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a2bc8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bc8-117">CommonParameters</span></span>
<span data-ttu-id="a2bc8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2bc8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bc8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2bc8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bc8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2bc8-120">INPUTS</span></span>

### <span data-ttu-id="a2bc8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a2bc8-121">System.String</span></span>

## <span data-ttu-id="a2bc8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2bc8-122">OUTPUTS</span></span>

### <span data-ttu-id="a2bc8-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="a2bc8-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="a2bc8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2bc8-124">NOTES</span></span>

## <span data-ttu-id="a2bc8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2bc8-125">RELATED LINKS</span></span>
