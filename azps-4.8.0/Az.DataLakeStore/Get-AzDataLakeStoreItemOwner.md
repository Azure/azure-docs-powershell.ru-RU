---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243064"
---
# <span data-ttu-id="fb250-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="fb250-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="fb250-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb250-102">SYNOPSIS</span></span>
<span data-ttu-id="fb250-103">Получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fb250-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fb250-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb250-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb250-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb250-105">DESCRIPTION</span></span>
<span data-ttu-id="fb250-106">Командлет **Get-AzDataLakeStoreItemOwner** получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fb250-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fb250-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb250-107">EXAMPLES</span></span>

### <span data-ttu-id="fb250-108">Пример 1: получение владельца для каталога</span><span class="sxs-lookup"><span data-stu-id="fb250-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="fb250-109">Эта команда получает владельца пользователя на корневой каталог учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="fb250-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="fb250-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb250-110">PARAMETERS</span></span>

### <span data-ttu-id="fb250-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fb250-111">-Account</span></span>
<span data-ttu-id="fb250-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fb250-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fb250-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb250-113">-DefaultProfile</span></span>
<span data-ttu-id="fb250-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb250-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb250-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fb250-115">-Path</span></span>
<span data-ttu-id="fb250-116">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="fb250-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb250-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fb250-117">-Type</span></span>
<span data-ttu-id="fb250-118">Указывает тип получаемого владельца.</span><span class="sxs-lookup"><span data-stu-id="fb250-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="fb250-119">Допустимые значения этого параметра: User и Group.</span><span class="sxs-lookup"><span data-stu-id="fb250-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb250-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb250-120">CommonParameters</span></span>
<span data-ttu-id="fb250-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb250-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb250-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb250-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb250-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb250-123">INPUTS</span></span>

### <span data-ttu-id="fb250-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fb250-124">System.String</span></span>

### <span data-ttu-id="fb250-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fb250-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fb250-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="fb250-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="fb250-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb250-127">OUTPUTS</span></span>

### <span data-ttu-id="fb250-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb250-128">System.String</span></span>

## <span data-ttu-id="fb250-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb250-129">NOTES</span></span>

## <span data-ttu-id="fb250-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb250-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb250-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="fb250-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


