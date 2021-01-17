---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400340"
---
# <span data-ttu-id="f4e25-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f4e25-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f4e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e25-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e25-103">Получает указанного надежного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4e25-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="f4e25-104">Если не указан поставщик, перечислены все поставщики для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f4e25-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="f4e25-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4e25-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e25-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4e25-106">DESCRIPTION</span></span>
<span data-ttu-id="f4e25-107">Cmdlet **Get-AzDataLakeStoreTrustedIdProvider** возвращает указанного надежного поставщика удостоверений в указанном магазине data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4e25-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="f4e25-108">Если поставщик не указан, перечислены все поставщики для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f4e25-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="f4e25-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4e25-109">EXAMPLES</span></span>

### <span data-ttu-id="f4e25-110">Пример 1. Получить определенного надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="f4e25-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="f4e25-111">Возвращает поставщика с именем MyProvider из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="f4e25-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="f4e25-112">Пример 2. Список всех поставщиков в учетной записи</span><span class="sxs-lookup"><span data-stu-id="f4e25-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="f4e25-113">Список всех поставщиков в учетной записи ContosoADL</span><span class="sxs-lookup"><span data-stu-id="f4e25-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="f4e25-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4e25-114">PARAMETERS</span></span>

### <span data-ttu-id="f4e25-115">-Account</span><span class="sxs-lookup"><span data-stu-id="f4e25-115">-Account</span></span>
<span data-ttu-id="f4e25-116">Учетная запись Data Lake Store для получения надежного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="f4e25-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="f4e25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e25-117">-DefaultProfile</span></span>
<span data-ttu-id="f4e25-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f4e25-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4e25-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f4e25-119">-Name</span></span>
<span data-ttu-id="f4e25-120">Имя надежного поставщика удостоверений, который нужно извлечь</span><span class="sxs-lookup"><span data-stu-id="f4e25-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="f4e25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e25-121">-ResourceGroupName</span></span>
<span data-ttu-id="f4e25-122">Имя группы ресурсов, под которой нужно получить указанного надежного поставщика удостоверений указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f4e25-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="f4e25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e25-123">CommonParameters</span></span>
<span data-ttu-id="f4e25-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e25-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e25-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e25-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4e25-126">INPUTS</span></span>

### <span data-ttu-id="f4e25-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f4e25-127">System.String</span></span>

## <span data-ttu-id="f4e25-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4e25-128">OUTPUTS</span></span>

### <span data-ttu-id="f4e25-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="f4e25-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="f4e25-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4e25-130">NOTES</span></span>

## <span data-ttu-id="f4e25-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4e25-131">RELATED LINKS</span></span>
