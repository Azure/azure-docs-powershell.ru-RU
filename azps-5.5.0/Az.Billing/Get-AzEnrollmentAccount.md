---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216073"
---
# <span data-ttu-id="75f50-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="75f50-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="75f50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f50-102">SYNOPSIS</span></span>
<span data-ttu-id="75f50-103">Получить учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="75f50-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="75f50-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75f50-104">SYNTAX</span></span>

### <span data-ttu-id="75f50-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75f50-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f50-106">Один</span><span class="sxs-lookup"><span data-stu-id="75f50-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f50-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75f50-107">DESCRIPTION</span></span>
<span data-ttu-id="75f50-108">Для **получения учетных записей регистрации возвращается cmdlet Get-AzEnrollmentAccount.**</span><span class="sxs-lookup"><span data-stu-id="75f50-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="75f50-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75f50-109">EXAMPLES</span></span>

### <span data-ttu-id="75f50-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75f50-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="75f50-111">Получить все доступные учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="75f50-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="75f50-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75f50-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="75f50-113">Получить учетную запись регистрации с указанным ид объекта.</span><span class="sxs-lookup"><span data-stu-id="75f50-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="75f50-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f50-114">PARAMETERS</span></span>

### <span data-ttu-id="75f50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f50-115">-DefaultProfile</span></span>
<span data-ttu-id="75f50-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75f50-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75f50-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="75f50-117">-ObjectId</span></span>
<span data-ttu-id="75f50-118">ObjectId определенной учетной записи регистрации, которая вам нужно получить.</span><span class="sxs-lookup"><span data-stu-id="75f50-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="75f50-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f50-119">CommonParameters</span></span>
<span data-ttu-id="75f50-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f50-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f50-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f50-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f50-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f50-122">INPUTS</span></span>

### <span data-ttu-id="75f50-123">Нет</span><span class="sxs-lookup"><span data-stu-id="75f50-123">None</span></span>

## <span data-ttu-id="75f50-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75f50-124">OUTPUTS</span></span>

### <span data-ttu-id="75f50-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="75f50-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="75f50-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75f50-126">NOTES</span></span>

## <span data-ttu-id="75f50-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75f50-127">RELATED LINKS</span></span>
