---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246488"
---
# <span data-ttu-id="c054a-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="c054a-101">Get-AzTenant</span></span>

## <span data-ttu-id="c054a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c054a-102">SYNOPSIS</span></span>
<span data-ttu-id="c054a-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c054a-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="c054a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c054a-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c054a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c054a-105">DESCRIPTION</span></span>
<span data-ttu-id="c054a-106">Командлет Get-AzTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c054a-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="c054a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c054a-107">EXAMPLES</span></span>

### <span data-ttu-id="c054a-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="c054a-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="c054a-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="c054a-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="c054a-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="c054a-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="c054a-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="c054a-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="c054a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c054a-112">PARAMETERS</span></span>

### <span data-ttu-id="c054a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c054a-113">-DefaultProfile</span></span>
<span data-ttu-id="c054a-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c054a-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c054a-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c054a-115">-TenantId</span></span>
<span data-ttu-id="c054a-116">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c054a-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c054a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c054a-117">CommonParameters</span></span>
<span data-ttu-id="c054a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c054a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c054a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c054a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c054a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c054a-120">INPUTS</span></span>

### <span data-ttu-id="c054a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c054a-121">System.String</span></span>

## <span data-ttu-id="c054a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c054a-122">OUTPUTS</span></span>

### <span data-ttu-id="c054a-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="c054a-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="c054a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c054a-124">NOTES</span></span>

## <span data-ttu-id="c054a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c054a-125">RELATED LINKS</span></span>
