---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: 07bcfff4ab8d1e071ed34c9a52e8aa4e98c32946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560924"
---
# <span data-ttu-id="8493c-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8493c-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8493c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8493c-102">SYNOPSIS</span></span>
<span data-ttu-id="8493c-103">Получает указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8493c-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="8493c-104">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8493c-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8493c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8493c-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8493c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8493c-106">DESCRIPTION</span></span>
<span data-ttu-id="8493c-107">Командлет **Get-AzureRmDataLakeStoreTrustedIdProvider** получает указанный доверенный поставщик удостоверений в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8493c-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="8493c-108">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8493c-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="8493c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8493c-109">EXAMPLES</span></span>

### <span data-ttu-id="8493c-110">Пример 1: получение определенного надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="8493c-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="8493c-111">Возвращает поставщик с именем "MyProvider" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8493c-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="8493c-112">Пример 2: список всех поставщиков в учетной записи</span><span class="sxs-lookup"><span data-stu-id="8493c-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="8493c-113">Список всех поставщиков в учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8493c-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="8493c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8493c-114">PARAMETERS</span></span>

### <span data-ttu-id="8493c-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8493c-115">-Account</span></span>
<span data-ttu-id="8493c-116">Учетная запись Data Lake Store для получения доверенного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="8493c-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="8493c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8493c-117">-DefaultProfile</span></span>
<span data-ttu-id="8493c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8493c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8493c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8493c-119">-Name</span></span>
<span data-ttu-id="8493c-120">Имя надежного поставщика удостоверений для извлечения</span><span class="sxs-lookup"><span data-stu-id="8493c-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="8493c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8493c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8493c-122">Имя группы ресурсов, в которой нужно получить доверенный поставщик удостоверений для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8493c-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="8493c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8493c-123">CommonParameters</span></span>
<span data-ttu-id="8493c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8493c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8493c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8493c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8493c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8493c-126">INPUTS</span></span>

### <span data-ttu-id="8493c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8493c-127">System.String</span></span>

## <span data-ttu-id="8493c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8493c-128">OUTPUTS</span></span>

### <span data-ttu-id="8493c-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="8493c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="8493c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8493c-130">NOTES</span></span>

## <span data-ttu-id="8493c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8493c-131">RELATED LINKS</span></span>
