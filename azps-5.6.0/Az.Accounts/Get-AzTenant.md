---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955032"
---
# <span data-ttu-id="69a56-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="69a56-101">Get-AzTenant</span></span>

## <span data-ttu-id="69a56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69a56-102">SYNOPSIS</span></span>
<span data-ttu-id="69a56-103">Клиенты, авторизованные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="69a56-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="69a56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69a56-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69a56-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69a56-105">DESCRIPTION</span></span>
<span data-ttu-id="69a56-106">С Get-AzTenant- и клиенты, авторизованные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="69a56-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="69a56-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69a56-107">EXAMPLES</span></span>

### <span data-ttu-id="69a56-108">Пример 1. Получение всех клиентов</span><span class="sxs-lookup"><span data-stu-id="69a56-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="69a56-109">В этом примере показано, как получить все авторизованные клиенты учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="69a56-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="69a56-110">Пример 2. Получение определенного клиента</span><span class="sxs-lookup"><span data-stu-id="69a56-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="69a56-111">В этом примере показано, как получить определенный авторизованный клиент учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="69a56-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="69a56-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69a56-112">PARAMETERS</span></span>

### <span data-ttu-id="69a56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69a56-113">-DefaultProfile</span></span>
<span data-ttu-id="69a56-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69a56-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69a56-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="69a56-115">-TenantId</span></span>
<span data-ttu-id="69a56-116">Определяет код клиента, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69a56-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69a56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a56-117">CommonParameters</span></span>
<span data-ttu-id="69a56-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69a56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a56-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69a56-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a56-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69a56-120">INPUTS</span></span>

### <span data-ttu-id="69a56-121">System.String</span><span class="sxs-lookup"><span data-stu-id="69a56-121">System.String</span></span>

## <span data-ttu-id="69a56-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69a56-122">OUTPUTS</span></span>

### <span data-ttu-id="69a56-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="69a56-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="69a56-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69a56-124">NOTES</span></span>

## <span data-ttu-id="69a56-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69a56-125">RELATED LINKS</span></span>
