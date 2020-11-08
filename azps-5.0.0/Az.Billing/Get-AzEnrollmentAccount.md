---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248420"
---
# <span data-ttu-id="8dad8-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="8dad8-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="8dad8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dad8-102">SYNOPSIS</span></span>
<span data-ttu-id="8dad8-103">Получение учетных записей регистрации.</span><span class="sxs-lookup"><span data-stu-id="8dad8-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="8dad8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dad8-104">SYNTAX</span></span>

### <span data-ttu-id="8dad8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dad8-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dad8-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="8dad8-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dad8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dad8-107">DESCRIPTION</span></span>
<span data-ttu-id="8dad8-108">Командлет **Get-AzEnrollmentAccount** получает учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="8dad8-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="8dad8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dad8-109">EXAMPLES</span></span>

### <span data-ttu-id="8dad8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dad8-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="8dad8-111">Получить все доступные учетные записи.</span><span class="sxs-lookup"><span data-stu-id="8dad8-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="8dad8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8dad8-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="8dad8-113">Получить учетную запись регистрации с указанным идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="8dad8-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="8dad8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dad8-114">PARAMETERS</span></span>

### <span data-ttu-id="8dad8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dad8-115">-DefaultProfile</span></span>
<span data-ttu-id="8dad8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8dad8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dad8-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8dad8-117">-ObjectId</span></span>
<span data-ttu-id="8dad8-118">ObjectId определенной учетной записи для получения.</span><span class="sxs-lookup"><span data-stu-id="8dad8-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="8dad8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dad8-119">CommonParameters</span></span>
<span data-ttu-id="8dad8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dad8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dad8-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dad8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dad8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dad8-122">INPUTS</span></span>

### <span data-ttu-id="8dad8-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="8dad8-123">None</span></span>

## <span data-ttu-id="8dad8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dad8-124">OUTPUTS</span></span>

### <span data-ttu-id="8dad8-125">Microsoft. Azure. Commands. Bill. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="8dad8-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="8dad8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dad8-126">NOTES</span></span>

## <span data-ttu-id="8dad8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dad8-127">RELATED LINKS</span></span>
