---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4276b9477e51165e01c716095d5f4e2a4ea6ca69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560927"
---
# <span data-ttu-id="44d8e-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="44d8e-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="44d8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="44d8e-103">Получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44d8e-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44d8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44d8e-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44d8e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="44d8e-106">Командлет **Get-AzureRmDataLakeStoreItemOwner** получает владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44d8e-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="44d8e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="44d8e-108">Пример 1: получение владельца для каталога</span><span class="sxs-lookup"><span data-stu-id="44d8e-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="44d8e-109">Эта команда получает владельца пользователя на корневой каталог учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="44d8e-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="44d8e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44d8e-110">PARAMETERS</span></span>

### <span data-ttu-id="44d8e-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="44d8e-111">-Account</span></span>
<span data-ttu-id="44d8e-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44d8e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="44d8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d8e-113">-DefaultProfile</span></span>
<span data-ttu-id="44d8e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44d8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44d8e-115">-Path</span><span class="sxs-lookup"><span data-stu-id="44d8e-115">-Path</span></span>
<span data-ttu-id="44d8e-116">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="44d8e-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="44d8e-117">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="44d8e-117">-Type</span></span>
<span data-ttu-id="44d8e-118">Указывает тип получаемого владельца.</span><span class="sxs-lookup"><span data-stu-id="44d8e-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="44d8e-119">Допустимые значения этого параметра: User и Group.</span><span class="sxs-lookup"><span data-stu-id="44d8e-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="44d8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d8e-120">CommonParameters</span></span>
<span data-ttu-id="44d8e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44d8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d8e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d8e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d8e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44d8e-123">INPUTS</span></span>

### <span data-ttu-id="44d8e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="44d8e-124">System.String</span></span>

### <span data-ttu-id="44d8e-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="44d8e-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="44d8e-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="44d8e-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="44d8e-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d8e-127">OUTPUTS</span></span>

### <span data-ttu-id="44d8e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="44d8e-128">System.String</span></span>
<span data-ttu-id="44d8e-129">Владелец указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="44d8e-129">The owner of the specified item.</span></span>

## <span data-ttu-id="44d8e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="44d8e-130">NOTES</span></span>

## <span data-ttu-id="44d8e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44d8e-131">RELATED LINKS</span></span>

[<span data-ttu-id="44d8e-132">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="44d8e-132">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


