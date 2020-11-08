---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080053"
---
# <span data-ttu-id="3d85b-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="3d85b-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="3d85b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d85b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d85b-103">Получение учетных записей регистрации.</span><span class="sxs-lookup"><span data-stu-id="3d85b-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="3d85b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d85b-104">SYNTAX</span></span>

### <span data-ttu-id="3d85b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d85b-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d85b-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="3d85b-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d85b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d85b-107">DESCRIPTION</span></span>
<span data-ttu-id="3d85b-108">Командлет **Get-AzEnrollmentAccount** получает учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="3d85b-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="3d85b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d85b-109">EXAMPLES</span></span>

### <span data-ttu-id="3d85b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d85b-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="3d85b-111">Получить все доступные учетные записи.</span><span class="sxs-lookup"><span data-stu-id="3d85b-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="3d85b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d85b-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="3d85b-113">Получить учетную запись регистрации с указанным идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="3d85b-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="3d85b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d85b-114">PARAMETERS</span></span>

### <span data-ttu-id="3d85b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d85b-115">-DefaultProfile</span></span>
<span data-ttu-id="3d85b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d85b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d85b-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3d85b-117">-ObjectId</span></span>
<span data-ttu-id="3d85b-118">ObjectId определенной учетной записи для получения.</span><span class="sxs-lookup"><span data-stu-id="3d85b-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="3d85b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d85b-119">CommonParameters</span></span>
<span data-ttu-id="3d85b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d85b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d85b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d85b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d85b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d85b-122">INPUTS</span></span>

### <span data-ttu-id="3d85b-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3d85b-123">None</span></span>

## <span data-ttu-id="3d85b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d85b-124">OUTPUTS</span></span>

### <span data-ttu-id="3d85b-125">Microsoft. Azure. Commands. Bill. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="3d85b-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="3d85b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d85b-126">NOTES</span></span>

## <span data-ttu-id="3d85b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d85b-127">RELATED LINKS</span></span>
