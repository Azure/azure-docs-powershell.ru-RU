---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222665"
---
# <span data-ttu-id="5885e-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5885e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5885e-102">SYNOPSIS</span></span>
<span data-ttu-id="5885e-103">Сведения об учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5885e-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5885e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5885e-104">SYNTAX</span></span>

### <span data-ttu-id="5885e-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5885e-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5885e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5885e-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5885e-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5885e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5885e-108">DESCRIPTION</span></span>
<span data-ttu-id="5885e-109">Для получения сведений о учетной записи Data Lake Store можно получить сведения о **cmdlet Get-AzDataLakeStoreAccount.**</span><span class="sxs-lookup"><span data-stu-id="5885e-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="5885e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5885e-110">EXAMPLES</span></span>

### <span data-ttu-id="5885e-111">Пример 1. Получить учетную запись Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5885e-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5885e-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5885e-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="5885e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5885e-113">PARAMETERS</span></span>

### <span data-ttu-id="5885e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5885e-114">-DefaultProfile</span></span>
<span data-ttu-id="5885e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5885e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5885e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5885e-116">-Name</span></span>
<span data-ttu-id="5885e-117">Указывает имя нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5885e-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="5885e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5885e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5885e-119">Имя группы ресурсов, которая содержит учетную запись Магазина данных, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5885e-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="5885e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5885e-120">CommonParameters</span></span>
<span data-ttu-id="5885e-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5885e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5885e-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5885e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5885e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5885e-123">INPUTS</span></span>

### <span data-ttu-id="5885e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5885e-124">System.String</span></span>

## <span data-ttu-id="5885e-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5885e-125">OUTPUTS</span></span>

### <span data-ttu-id="5885e-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDAtaLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="5885e-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5885e-127">NOTES</span></span>

## <span data-ttu-id="5885e-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5885e-128">RELATED LINKS</span></span>

[<span data-ttu-id="5885e-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5885e-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5885e-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5885e-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5885e-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


