---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313340"
---
# <span data-ttu-id="6cb53-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6cb53-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6cb53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cb53-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb53-103">Получает указанного доверенного поставщика удостоверений в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6cb53-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="6cb53-104">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6cb53-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="6cb53-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cb53-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb53-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cb53-106">DESCRIPTION</span></span>
<span data-ttu-id="6cb53-107">Командлет **Get-AzDataLakeStoreTrustedIdProvider** получает указанный доверенный поставщик удостоверений в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6cb53-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="6cb53-108">Если поставщик не указан, выводит список всех поставщиков для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6cb53-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="6cb53-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cb53-109">EXAMPLES</span></span>

### <span data-ttu-id="6cb53-110">Пример 1: получение определенного надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="6cb53-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="6cb53-111">Возвращает поставщик с именем "MyProvider" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="6cb53-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="6cb53-112">Пример 2: список всех поставщиков в учетной записи</span><span class="sxs-lookup"><span data-stu-id="6cb53-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="6cb53-113">Список всех поставщиков в учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="6cb53-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="6cb53-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cb53-114">PARAMETERS</span></span>

### <span data-ttu-id="6cb53-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6cb53-115">-Account</span></span>
<span data-ttu-id="6cb53-116">Учетная запись Data Lake Store для получения доверенного поставщика удостоверений из</span><span class="sxs-lookup"><span data-stu-id="6cb53-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="6cb53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb53-117">-DefaultProfile</span></span>
<span data-ttu-id="6cb53-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6cb53-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6cb53-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cb53-119">-Name</span></span>
<span data-ttu-id="6cb53-120">Имя надежного поставщика удостоверений для извлечения</span><span class="sxs-lookup"><span data-stu-id="6cb53-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="6cb53-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb53-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cb53-122">Имя группы ресурсов, в которой нужно получить доверенный поставщик удостоверений для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6cb53-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="6cb53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb53-123">CommonParameters</span></span>
<span data-ttu-id="6cb53-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cb53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb53-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb53-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cb53-126">INPUTS</span></span>

### <span data-ttu-id="6cb53-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6cb53-127">System.String</span></span>

## <span data-ttu-id="6cb53-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cb53-128">OUTPUTS</span></span>

### <span data-ttu-id="6cb53-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="6cb53-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="6cb53-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cb53-130">NOTES</span></span>

## <span data-ttu-id="6cb53-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cb53-131">RELATED LINKS</span></span>
