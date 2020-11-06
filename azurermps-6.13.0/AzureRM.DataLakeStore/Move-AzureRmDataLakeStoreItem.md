---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 15c516e1d54b6e706176ceb28a1974e848945c47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560911"
---
# <span data-ttu-id="fc5f1-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="fc5f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5f1-103">Перемещение или переименование файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc5f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc5f1-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5f1-106">Командлет **Move-AzureRmDataLakeStoreItem** перемещает или переименовывает файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc5f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="fc5f1-108">Пример 1: перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="fc5f1-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="fc5f1-109">Эта команда переименовывает элемент File.txt в RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="fc5f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="fc5f1-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-111">-Account</span></span>
<span data-ttu-id="fc5f1-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fc5f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5f1-113">-DefaultProfile</span></span>
<span data-ttu-id="fc5f1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc5f1-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="fc5f1-115">-Destination</span></span>
<span data-ttu-id="fc5f1-116">Указывает путь к Data Lake Store, куда нужно переместить элемент, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fc5f1-117">-Force</span></span>
<span data-ttu-id="fc5f1-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-119">-Path</span><span class="sxs-lookup"><span data-stu-id="fc5f1-119">-Path</span></span>
<span data-ttu-id="fc5f1-120">Указывает путь к Data Lake Store для элемента, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fc5f1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc5f1-121">-Confirm</span></span>
<span data-ttu-id="fc5f1-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5f1-123">-WhatIf</span></span>
<span data-ttu-id="fc5f1-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5f1-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5f1-126">CommonParameters</span></span>
<span data-ttu-id="fc5f1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5f1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5f1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc5f1-129">INPUTS</span></span>

### <span data-ttu-id="fc5f1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5f1-130">System.String</span></span>

### <span data-ttu-id="fc5f1-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fc5f1-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fc5f1-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc5f1-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc5f1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc5f1-133">OUTPUTS</span></span>

### <span data-ttu-id="fc5f1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5f1-134">System.String</span></span>
<span data-ttu-id="fc5f1-135">Полный путь к перемещенному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-135">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="fc5f1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc5f1-136">NOTES</span></span>

## <span data-ttu-id="fc5f1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc5f1-137">RELATED LINKS</span></span>

[<span data-ttu-id="fc5f1-138">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-138">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc5f1-139">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-139">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc5f1-140">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-140">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc5f1-141">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-141">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc5f1-142">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-142">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fc5f1-143">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fc5f1-143">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


