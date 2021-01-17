---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417287"
---
# <span data-ttu-id="4a537-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="4a537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a537-102">SYNOPSIS</span></span>
<span data-ttu-id="4a537-103">Сведения об учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a537-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="4a537-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a537-104">SYNTAX</span></span>

### <span data-ttu-id="4a537-105">GetAllInSubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a537-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a537-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a537-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a537-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a537-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a537-108">DESCRIPTION</span></span>
<span data-ttu-id="4a537-109">Для получения сведений о учетной записи Data Lake Store можно получить сведения о **cmdlet Get-AzDataLakeStoreAccount.**</span><span class="sxs-lookup"><span data-stu-id="4a537-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="4a537-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a537-110">EXAMPLES</span></span>

### <span data-ttu-id="4a537-111">Пример 1. Получить учетную запись Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4a537-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="4a537-112">Эта команда получает учетную запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="4a537-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="4a537-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a537-113">PARAMETERS</span></span>

### <span data-ttu-id="4a537-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a537-114">-DefaultProfile</span></span>
<span data-ttu-id="4a537-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a537-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a537-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4a537-116">-Name</span></span>
<span data-ttu-id="4a537-117">Указывает имя нужной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4a537-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="4a537-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a537-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a537-119">Имя группы ресурсов, которая содержит учетную запись Магазина данных, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="4a537-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="4a537-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a537-120">CommonParameters</span></span>
<span data-ttu-id="4a537-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a537-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a537-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a537-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a537-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a537-123">INPUTS</span></span>

### <span data-ttu-id="4a537-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4a537-124">System.String</span></span>

## <span data-ttu-id="4a537-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a537-125">OUTPUTS</span></span>

### <span data-ttu-id="4a537-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDAtaLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="4a537-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a537-127">NOTES</span></span>

## <span data-ttu-id="4a537-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a537-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a537-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4a537-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4a537-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4a537-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4a537-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


