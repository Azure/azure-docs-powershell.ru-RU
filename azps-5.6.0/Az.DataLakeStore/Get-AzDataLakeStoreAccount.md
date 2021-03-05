---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963096"
---
# <span data-ttu-id="2a9d6-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="2a9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9d6-103">Сведения об учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2a9d6-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="2a9d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a9d6-104">SYNTAX</span></span>

### <span data-ttu-id="2a9d6-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a9d6-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a9d6-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a9d6-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a9d6-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a9d6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a9d6-108">DESCRIPTION</span></span>
<span data-ttu-id="2a9d6-109">Для получения сведений о учетной записи Data Lake Store можно получить сведения о **cmdlet Get-AzDataLakeStoreAccount.**</span><span class="sxs-lookup"><span data-stu-id="2a9d6-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="2a9d6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a9d6-110">EXAMPLES</span></span>

### <span data-ttu-id="2a9d6-111">Пример 1. Получить учетную запись Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="2a9d6-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="2a9d6-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="2a9d6-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="2a9d6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a9d6-113">PARAMETERS</span></span>

### <span data-ttu-id="2a9d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9d6-114">-DefaultProfile</span></span>
<span data-ttu-id="2a9d6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2a9d6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a9d6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2a9d6-116">-Name</span></span>
<span data-ttu-id="2a9d6-117">Указывает имя нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2a9d6-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="2a9d6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9d6-118">-ResourceGroupName</span></span>
<span data-ttu-id="2a9d6-119">Имя группы ресурсов, которая содержит учетную запись Магазина данных, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2a9d6-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="2a9d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9d6-120">CommonParameters</span></span>
<span data-ttu-id="2a9d6-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9d6-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a9d6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9d6-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a9d6-123">INPUTS</span></span>

### <span data-ttu-id="2a9d6-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2a9d6-124">System.String</span></span>

## <span data-ttu-id="2a9d6-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a9d6-125">OUTPUTS</span></span>

### <span data-ttu-id="2a9d6-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDAtaLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="2a9d6-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a9d6-127">NOTES</span></span>

## <span data-ttu-id="2a9d6-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a9d6-128">RELATED LINKS</span></span>

[<span data-ttu-id="2a9d6-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2a9d6-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2a9d6-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="2a9d6-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2a9d6-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


