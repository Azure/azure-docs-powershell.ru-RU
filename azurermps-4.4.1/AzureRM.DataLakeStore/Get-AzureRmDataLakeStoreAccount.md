---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559828"
---
# <span data-ttu-id="2c909-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="2c909-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c909-102">SYNOPSIS</span></span>
<span data-ttu-id="2c909-103">Получение сведений об учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c909-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c909-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c909-104">SYNTAX</span></span>

### <span data-ttu-id="2c909-105">Все в подписке (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c909-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c909-106">Все в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c909-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c909-107">Конкретный счет</span><span class="sxs-lookup"><span data-stu-id="2c909-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c909-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c909-108">DESCRIPTION</span></span>
<span data-ttu-id="2c909-109">Командлет **Get-AzureRmDataLakeStoreAccount** получает сведения о учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c909-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="2c909-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c909-110">EXAMPLES</span></span>

### <span data-ttu-id="2c909-111">Пример 1: получение учетной записи для Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="2c909-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="2c909-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="2c909-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="2c909-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c909-113">PARAMETERS</span></span>

### <span data-ttu-id="2c909-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c909-114">-Name</span></span>
<span data-ttu-id="2c909-115">Указывает имя учетной записи, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2c909-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c909-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c909-116">-ResourceGroupName</span></span>
<span data-ttu-id="2c909-117">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2c909-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c909-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c909-118">-DefaultProfile</span></span>
<span data-ttu-id="2c909-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c909-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c909-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c909-120">CommonParameters</span></span>
<span data-ttu-id="2c909-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c909-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c909-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c909-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c909-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c909-123">INPUTS</span></span>

## <span data-ttu-id="2c909-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c909-124">OUTPUTS</span></span>

### <span data-ttu-id="2c909-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="2c909-126">Указанная учетная запись Data Lake Store запросите ее.</span><span class="sxs-lookup"><span data-stu-id="2c909-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="2c909-127">Список<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="2c909-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="2c909-128">Список учетных записей Data Lake Store в указанной группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="2c909-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="2c909-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c909-129">NOTES</span></span>

## <span data-ttu-id="2c909-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c909-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c909-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="2c909-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="2c909-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="2c909-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2c909-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


