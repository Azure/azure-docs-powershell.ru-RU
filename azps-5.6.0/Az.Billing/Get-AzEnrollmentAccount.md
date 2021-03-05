---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992928"
---
# <span data-ttu-id="93f86-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="93f86-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="93f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f86-102">SYNOPSIS</span></span>
<span data-ttu-id="93f86-103">Получить учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="93f86-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="93f86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93f86-104">SYNTAX</span></span>

### <span data-ttu-id="93f86-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93f86-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93f86-106">Один</span><span class="sxs-lookup"><span data-stu-id="93f86-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f86-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93f86-107">DESCRIPTION</span></span>
<span data-ttu-id="93f86-108">Для **получения учетных записей регистрации возвращается cmdlet Get-AzEnrollmentAccount.**</span><span class="sxs-lookup"><span data-stu-id="93f86-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="93f86-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93f86-109">EXAMPLES</span></span>

### <span data-ttu-id="93f86-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93f86-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="93f86-111">Получить все доступные учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="93f86-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="93f86-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="93f86-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="93f86-113">Получить учетную запись регистрации с указанным ид объекта.</span><span class="sxs-lookup"><span data-stu-id="93f86-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="93f86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f86-114">PARAMETERS</span></span>

### <span data-ttu-id="93f86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f86-115">-DefaultProfile</span></span>
<span data-ttu-id="93f86-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="93f86-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f86-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93f86-117">-ObjectId</span></span>
<span data-ttu-id="93f86-118">ObjectId определенной учетной записи регистрации, которая вам нужно получить.</span><span class="sxs-lookup"><span data-stu-id="93f86-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f86-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f86-119">CommonParameters</span></span>
<span data-ttu-id="93f86-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f86-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f86-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f86-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f86-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93f86-122">INPUTS</span></span>

### <span data-ttu-id="93f86-123">Нет</span><span class="sxs-lookup"><span data-stu-id="93f86-123">None</span></span>

## <span data-ttu-id="93f86-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93f86-124">OUTPUTS</span></span>

### <span data-ttu-id="93f86-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="93f86-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="93f86-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93f86-126">NOTES</span></span>

## <span data-ttu-id="93f86-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93f86-127">RELATED LINKS</span></span>
