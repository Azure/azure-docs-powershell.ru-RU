---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559280"
---
# <span data-ttu-id="49a26-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="49a26-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="49a26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49a26-102">SYNOPSIS</span></span>
<span data-ttu-id="49a26-103">Получение учетных записей регистрации.</span><span class="sxs-lookup"><span data-stu-id="49a26-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49a26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49a26-104">SYNTAX</span></span>

### <span data-ttu-id="49a26-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49a26-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a26-106">Единственное</span><span class="sxs-lookup"><span data-stu-id="49a26-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a26-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49a26-107">DESCRIPTION</span></span>
<span data-ttu-id="49a26-108">Командлет **Get-AzureRmEnrollmentAccount** получает учетные записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="49a26-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="49a26-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49a26-109">EXAMPLES</span></span>

### <span data-ttu-id="49a26-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49a26-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="49a26-111">Получить все доступные учетные записи.</span><span class="sxs-lookup"><span data-stu-id="49a26-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="49a26-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49a26-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="49a26-113">Получить учетную запись регистрации с указанным идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="49a26-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="49a26-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49a26-114">PARAMETERS</span></span>

### <span data-ttu-id="49a26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a26-115">-DefaultProfile</span></span>
<span data-ttu-id="49a26-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="49a26-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a26-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49a26-117">-ObjectId</span></span>
<span data-ttu-id="49a26-118">ObjectId определенной учетной записи для получения.</span><span class="sxs-lookup"><span data-stu-id="49a26-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a26-119">CommonParameters</span></span>
<span data-ttu-id="49a26-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49a26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a26-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a26-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a26-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49a26-122">INPUTS</span></span>

### <span data-ttu-id="49a26-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="49a26-123">None</span></span>

## <span data-ttu-id="49a26-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49a26-124">OUTPUTS</span></span>

### <span data-ttu-id="49a26-125">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. выставление PSEnrollmentAccount, версия = 0.14.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="49a26-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="49a26-126">Microsoft. Azure. Commands. Bill. Models. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="49a26-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="49a26-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="49a26-127">NOTES</span></span>

## <span data-ttu-id="49a26-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49a26-128">RELATED LINKS</span></span>

