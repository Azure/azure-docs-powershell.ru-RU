---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4806c4c25ac6fecce4961ef5d4ffe44daa1ae8f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567014"
---
# <span data-ttu-id="d8d34-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d8d34-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="d8d34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8d34-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d34-103">Изменение владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8d34-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8d34-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d34-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d34-106">Командлет **Set-AzureRmDataLakeStoreItemOwner** изменяет владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8d34-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d8d34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8d34-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d34-108">Пример 1: назначение владельца элемента</span><span class="sxs-lookup"><span data-stu-id="d8d34-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d8d34-109">Эта команда задает для владельца корневого каталога значение Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="d8d34-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="d8d34-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8d34-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d34-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d8d34-111">-Account</span></span>
<span data-ttu-id="d8d34-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d8d34-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d34-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d34-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d34-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-115">-ID</span><span class="sxs-lookup"><span data-stu-id="d8d34-115">-Id</span></span>
<span data-ttu-id="d8d34-116">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, который будет использоваться в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="d8d34-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8d34-117">-PassThru</span></span>
<span data-ttu-id="d8d34-118">Указывает, что должен возвращаться конечный обновленный владелец.</span><span class="sxs-lookup"><span data-stu-id="d8d34-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d8d34-119">-Path</span></span>
<span data-ttu-id="d8d34-120">Указывает путь к Data Lake Store для элемента, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d8d34-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="d8d34-121">-Type</span></span>
<span data-ttu-id="d8d34-122">Указывает тип владельца для задания.</span><span class="sxs-lookup"><span data-stu-id="d8d34-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="d8d34-123">Допустимые значения этого параметра: User и Group.</span><span class="sxs-lookup"><span data-stu-id="d8d34-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d34-124">-Confirm</span></span>
<span data-ttu-id="d8d34-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8d34-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d34-126">-WhatIf</span></span>
<span data-ttu-id="d8d34-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8d34-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d34-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8d34-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d34-129">CommonParameters</span></span>
<span data-ttu-id="d8d34-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8d34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d34-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d34-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d34-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8d34-132">INPUTS</span></span>

### <span data-ttu-id="d8d34-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8d34-133">None</span></span>
<span data-ttu-id="d8d34-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d8d34-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8d34-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8d34-135">OUTPUTS</span></span>

### <span data-ttu-id="d8d34-136">подстрок</span><span class="sxs-lookup"><span data-stu-id="d8d34-136">string</span></span>
<span data-ttu-id="d8d34-137">Если указана функция PassThru, возвращает обновленный владелец.</span><span class="sxs-lookup"><span data-stu-id="d8d34-137">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="d8d34-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8d34-138">NOTES</span></span>

## <span data-ttu-id="d8d34-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8d34-139">RELATED LINKS</span></span>

[<span data-ttu-id="d8d34-140">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d8d34-140">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


