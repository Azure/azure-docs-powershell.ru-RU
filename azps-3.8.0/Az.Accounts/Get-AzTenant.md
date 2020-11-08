---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4a39853cfaabbee6dc6e9e87e7c504db2f8d53ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065399"
---
# <span data-ttu-id="93f15-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="93f15-101">Get-AzTenant</span></span>

## <span data-ttu-id="93f15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93f15-102">SYNOPSIS</span></span>
<span data-ttu-id="93f15-103">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="93f15-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="93f15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93f15-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f15-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93f15-105">DESCRIPTION</span></span>
<span data-ttu-id="93f15-106">Командлет Get-AzTenant получает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="93f15-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="93f15-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93f15-107">EXAMPLES</span></span>

### <span data-ttu-id="93f15-108">Пример 1: Загрузка всех клиентов</span><span class="sxs-lookup"><span data-stu-id="93f15-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="93f15-109">В этом примере показано, как получить всех авторизованных клиентов учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="93f15-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="93f15-110">Пример 2: как относящихся к определенному клиенту</span><span class="sxs-lookup"><span data-stu-id="93f15-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="93f15-111">В этом примере показано, как получить определенного авторизованного клиента учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="93f15-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="93f15-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93f15-112">PARAMETERS</span></span>

### <span data-ttu-id="93f15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f15-113">-DefaultProfile</span></span>
<span data-ttu-id="93f15-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="93f15-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f15-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="93f15-115">-TenantId</span></span>
<span data-ttu-id="93f15-116">Указывает идентификатор клиента, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="93f15-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="93f15-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f15-117">CommonParameters</span></span>
<span data-ttu-id="93f15-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93f15-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f15-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f15-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f15-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93f15-120">INPUTS</span></span>

### <span data-ttu-id="93f15-121">System. String</span><span class="sxs-lookup"><span data-stu-id="93f15-121">System.String</span></span>

## <span data-ttu-id="93f15-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93f15-122">OUTPUTS</span></span>

### <span data-ttu-id="93f15-123">Microsoft. Azure. Commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="93f15-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="93f15-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="93f15-124">NOTES</span></span>

## <span data-ttu-id="93f15-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93f15-125">RELATED LINKS</span></span>
