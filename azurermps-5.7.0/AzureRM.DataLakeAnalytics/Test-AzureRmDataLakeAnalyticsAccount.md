---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559084"
---
# <span data-ttu-id="db66a-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="db66a-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="db66a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db66a-102">SYNOPSIS</span></span>
<span data-ttu-id="db66a-103">Проверка наличия учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="db66a-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db66a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db66a-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db66a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db66a-105">DESCRIPTION</span></span>
<span data-ttu-id="db66a-106">Командлет **Test-AzureRmDataLakeAnalyticsAccount** проверяет наличие учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="db66a-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="db66a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db66a-107">EXAMPLES</span></span>

### <span data-ttu-id="db66a-108">Пример 1: Проверка наличия учетной записи</span><span class="sxs-lookup"><span data-stu-id="db66a-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="db66a-109">Эта команда проверяет, существует ли учетная запись с именем ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="db66a-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="db66a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db66a-110">PARAMETERS</span></span>

### <span data-ttu-id="db66a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db66a-111">-DefaultProfile</span></span>
<span data-ttu-id="db66a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db66a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db66a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db66a-113">-Name</span></span>
<span data-ttu-id="db66a-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="db66a-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db66a-115">-ResourceGroupName</span></span>
<span data-ttu-id="db66a-116">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="db66a-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db66a-117">CommonParameters</span></span>
<span data-ttu-id="db66a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db66a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db66a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db66a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db66a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db66a-120">INPUTS</span></span>

### <span data-ttu-id="db66a-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="db66a-121">None</span></span>
<span data-ttu-id="db66a-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="db66a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db66a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db66a-123">OUTPUTS</span></span>

### <span data-ttu-id="db66a-124">логических</span><span class="sxs-lookup"><span data-stu-id="db66a-124">bool</span></span>
<span data-ttu-id="db66a-125">Значение true или false указывает, существует ли учетная запись или нет.</span><span class="sxs-lookup"><span data-stu-id="db66a-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="db66a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="db66a-126">NOTES</span></span>

## <span data-ttu-id="db66a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db66a-127">RELATED LINKS</span></span>

[<span data-ttu-id="db66a-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="db66a-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="db66a-129">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="db66a-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="db66a-130">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="db66a-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


