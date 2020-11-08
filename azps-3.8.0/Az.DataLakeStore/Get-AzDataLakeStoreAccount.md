---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064976"
---
# <span data-ttu-id="5d346-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5d346-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d346-102">SYNOPSIS</span></span>
<span data-ttu-id="5d346-103">Получение сведений об учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d346-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5d346-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d346-104">SYNTAX</span></span>

### <span data-ttu-id="5d346-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d346-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d346-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d346-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d346-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d346-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d346-108">DESCRIPTION</span></span>
<span data-ttu-id="5d346-109">Командлет **Get-AzDataLakeStoreAccount** получает сведения о учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5d346-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5d346-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d346-110">EXAMPLES</span></span>

### <span data-ttu-id="5d346-111">Пример 1: получение учетной записи для Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5d346-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5d346-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5d346-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="5d346-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d346-113">PARAMETERS</span></span>

### <span data-ttu-id="5d346-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d346-114">-DefaultProfile</span></span>
<span data-ttu-id="5d346-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5d346-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d346-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d346-116">-Name</span></span>
<span data-ttu-id="5d346-117">Указывает имя учетной записи, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5d346-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="5d346-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d346-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d346-119">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5d346-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="5d346-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d346-120">CommonParameters</span></span>
<span data-ttu-id="5d346-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d346-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d346-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d346-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d346-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d346-123">INPUTS</span></span>

### <span data-ttu-id="5d346-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5d346-124">System.String</span></span>

## <span data-ttu-id="5d346-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d346-125">OUTPUTS</span></span>

### <span data-ttu-id="5d346-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="5d346-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d346-127">NOTES</span></span>

## <span data-ttu-id="5d346-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d346-128">RELATED LINKS</span></span>

[<span data-ttu-id="5d346-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5d346-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5d346-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5d346-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5d346-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


