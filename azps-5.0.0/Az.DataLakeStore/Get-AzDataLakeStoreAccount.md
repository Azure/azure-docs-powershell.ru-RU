---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313400"
---
# <span data-ttu-id="dd7b9-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="dd7b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7b9-103">Получение сведений об учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="dd7b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd7b9-104">SYNTAX</span></span>

### <span data-ttu-id="dd7b9-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd7b9-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7b9-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dd7b9-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd7b9-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd7b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd7b9-108">DESCRIPTION</span></span>
<span data-ttu-id="dd7b9-109">Командлет **Get-AzDataLakeStoreAccount** получает сведения о учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="dd7b9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd7b9-110">EXAMPLES</span></span>

### <span data-ttu-id="dd7b9-111">Пример 1: получение учетной записи для Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="dd7b9-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="dd7b9-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="dd7b9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd7b9-113">PARAMETERS</span></span>

### <span data-ttu-id="dd7b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7b9-114">-DefaultProfile</span></span>
<span data-ttu-id="dd7b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd7b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd7b9-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd7b9-116">-Name</span></span>
<span data-ttu-id="dd7b9-117">Указывает имя учетной записи, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="dd7b9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7b9-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd7b9-119">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="dd7b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7b9-120">CommonParameters</span></span>
<span data-ttu-id="dd7b9-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd7b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7b9-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd7b9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7b9-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd7b9-123">INPUTS</span></span>

### <span data-ttu-id="dd7b9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dd7b9-124">System.String</span></span>

## <span data-ttu-id="dd7b9-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd7b9-125">OUTPUTS</span></span>

### <span data-ttu-id="dd7b9-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="dd7b9-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd7b9-127">NOTES</span></span>

## <span data-ttu-id="dd7b9-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd7b9-128">RELATED LINKS</span></span>

[<span data-ttu-id="dd7b9-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dd7b9-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dd7b9-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dd7b9-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dd7b9-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


