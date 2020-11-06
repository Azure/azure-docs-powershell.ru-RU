---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556704"
---
# <span data-ttu-id="bf341-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="bf341-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf341-102">SYNOPSIS</span></span>
<span data-ttu-id="bf341-103">Получение сведений об учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bf341-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf341-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf341-104">SYNTAX</span></span>

### <span data-ttu-id="bf341-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf341-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf341-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf341-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf341-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf341-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf341-108">DESCRIPTION</span></span>
<span data-ttu-id="bf341-109">Командлет **Get-AzureRmDataLakeStoreAccount** получает сведения о учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bf341-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="bf341-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf341-110">EXAMPLES</span></span>

### <span data-ttu-id="bf341-111">Пример 1: получение учетной записи для Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bf341-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="bf341-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="bf341-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="bf341-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf341-113">PARAMETERS</span></span>

### <span data-ttu-id="bf341-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf341-114">-DefaultProfile</span></span>
<span data-ttu-id="bf341-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bf341-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf341-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf341-116">-Name</span></span>
<span data-ttu-id="bf341-117">Указывает имя учетной записи, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bf341-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf341-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf341-119">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bf341-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf341-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf341-120">CommonParameters</span></span>
<span data-ttu-id="bf341-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf341-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf341-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf341-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf341-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf341-123">INPUTS</span></span>

### <span data-ttu-id="bf341-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bf341-124">System.String</span></span>

## <span data-ttu-id="bf341-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf341-125">OUTPUTS</span></span>

### <span data-ttu-id="bf341-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="bf341-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf341-127">NOTES</span></span>

## <span data-ttu-id="bf341-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf341-128">RELATED LINKS</span></span>

[<span data-ttu-id="bf341-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="bf341-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="bf341-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="bf341-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bf341-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


