---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400964"
---
# <span data-ttu-id="32eca-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="32eca-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="32eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32eca-102">SYNOPSIS</span></span>
<span data-ttu-id="32eca-103">Получить учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="32eca-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="32eca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32eca-104">SYNTAX</span></span>

### <span data-ttu-id="32eca-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32eca-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eca-106">Один</span><span class="sxs-lookup"><span data-stu-id="32eca-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32eca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32eca-107">DESCRIPTION</span></span>
<span data-ttu-id="32eca-108">Для **получения учетных записей регистрации возвращается cmdlet Get-AzEnrollmentAccount.**</span><span class="sxs-lookup"><span data-stu-id="32eca-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="32eca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32eca-109">EXAMPLES</span></span>

### <span data-ttu-id="32eca-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32eca-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="32eca-111">Получить все доступные учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="32eca-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="32eca-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32eca-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="32eca-113">Получить учетную запись регистрации с указанным ид объекта.</span><span class="sxs-lookup"><span data-stu-id="32eca-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="32eca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32eca-114">PARAMETERS</span></span>

### <span data-ttu-id="32eca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eca-115">-DefaultProfile</span></span>
<span data-ttu-id="32eca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32eca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32eca-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32eca-117">-ObjectId</span></span>
<span data-ttu-id="32eca-118">ObjectId определенной учетной записи регистрации, которая вам нужно получить.</span><span class="sxs-lookup"><span data-stu-id="32eca-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="32eca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eca-119">CommonParameters</span></span>
<span data-ttu-id="32eca-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32eca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eca-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32eca-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eca-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32eca-122">INPUTS</span></span>

### <span data-ttu-id="32eca-123">Нет</span><span class="sxs-lookup"><span data-stu-id="32eca-123">None</span></span>

## <span data-ttu-id="32eca-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32eca-124">OUTPUTS</span></span>

### <span data-ttu-id="32eca-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="32eca-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="32eca-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32eca-126">NOTES</span></span>

## <span data-ttu-id="32eca-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32eca-127">RELATED LINKS</span></span>
