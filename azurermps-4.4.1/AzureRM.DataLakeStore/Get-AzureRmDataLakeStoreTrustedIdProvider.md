---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567653"
---
# <span data-ttu-id="7d2e5-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7d2e5-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="7d2e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d2e5-103">Получает указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7d2e5-104">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d2e5-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d2e5-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d2e5-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d2e5-106">DESCRIPTION</span></span>
<span data-ttu-id="7d2e5-107">Командлет **Get-AzureRmDataLakeStoreTrustedIdProvider** получает указанный доверенный поставщик удостоверений в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="7d2e5-108">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="7d2e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d2e5-109">EXAMPLES</span></span>

### <span data-ttu-id="7d2e5-110">Пример 1: получение определенного надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="7d2e5-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="7d2e5-111">Возвращает поставщик с именем "MyProvider" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="7d2e5-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="7d2e5-112">Пример 2: список всех поставщиков в учетной записи</span><span class="sxs-lookup"><span data-stu-id="7d2e5-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="7d2e5-113">Список всех поставщиков в учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="7d2e5-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="7d2e5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d2e5-114">PARAMETERS</span></span>

### <span data-ttu-id="7d2e5-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-115">-Account</span></span>
<span data-ttu-id="7d2e5-116">Учетная запись Data Lake Store для получения доверенного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="7d2e5-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2e5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d2e5-117">-Name</span></span>
<span data-ttu-id="7d2e5-118">Имя надежного поставщика удостоверений для извлечения</span><span class="sxs-lookup"><span data-stu-id="7d2e5-118">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d2e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d2e5-120">Имя группы ресурсов, в которой нужно получить доверенный поставщик удостоверений для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d2e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d2e5-121">-DefaultProfile</span></span>
<span data-ttu-id="7d2e5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d2e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d2e5-123">CommonParameters</span></span>
<span data-ttu-id="7d2e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d2e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d2e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d2e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d2e5-126">INPUTS</span></span>

## <span data-ttu-id="7d2e5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d2e5-127">OUTPUTS</span></span>

### <span data-ttu-id="7d2e5-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="7d2e5-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="7d2e5-129">Сведения о указанном надежном поставщике удостоверений.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="7d2e5-130">Оставлял<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="7d2e5-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="7d2e5-131">Список доверенных поставщиков удостоверений в указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7d2e5-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="7d2e5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d2e5-132">NOTES</span></span>

## <span data-ttu-id="7d2e5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d2e5-133">RELATED LINKS</span></span>

