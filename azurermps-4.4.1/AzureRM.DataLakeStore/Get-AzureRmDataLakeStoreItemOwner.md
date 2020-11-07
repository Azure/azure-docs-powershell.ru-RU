---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733752"
---
# <span data-ttu-id="22265-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="22265-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="22265-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22265-102">SYNOPSIS</span></span>
<span data-ttu-id="22265-103">Получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22265-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22265-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22265-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22265-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22265-105">DESCRIPTION</span></span>
<span data-ttu-id="22265-106">Командлет **Get-AzureRmDataLakeStoreItemOwner** получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22265-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="22265-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22265-107">EXAMPLES</span></span>

### <span data-ttu-id="22265-108">Пример 1: получение владельца для каталога</span><span class="sxs-lookup"><span data-stu-id="22265-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="22265-109">Эта команда получает владельца пользователя на корневой каталог учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="22265-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="22265-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22265-110">PARAMETERS</span></span>

### <span data-ttu-id="22265-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="22265-111">-Account</span></span>
<span data-ttu-id="22265-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="22265-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="22265-113">-Path</span><span class="sxs-lookup"><span data-stu-id="22265-113">-Path</span></span>
<span data-ttu-id="22265-114">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="22265-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="22265-115">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="22265-115">-Type</span></span>
<span data-ttu-id="22265-116">Указывает тип получаемого владельца.</span><span class="sxs-lookup"><span data-stu-id="22265-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="22265-117">Допустимые значения этого параметра: User и Group.</span><span class="sxs-lookup"><span data-stu-id="22265-117">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="22265-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22265-118">-DefaultProfile</span></span>
<span data-ttu-id="22265-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22265-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22265-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22265-120">CommonParameters</span></span>
<span data-ttu-id="22265-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22265-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22265-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22265-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22265-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22265-123">INPUTS</span></span>

## <span data-ttu-id="22265-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22265-124">OUTPUTS</span></span>

### <span data-ttu-id="22265-125">подстрок</span><span class="sxs-lookup"><span data-stu-id="22265-125">string</span></span>
<span data-ttu-id="22265-126">Владелец указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="22265-126">The owner of the specified item.</span></span>

## <span data-ttu-id="22265-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="22265-127">NOTES</span></span>

## <span data-ttu-id="22265-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22265-128">RELATED LINKS</span></span>

[<span data-ttu-id="22265-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="22265-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


