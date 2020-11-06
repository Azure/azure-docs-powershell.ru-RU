---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557371"
---
# <span data-ttu-id="ee24a-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ee24a-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="ee24a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee24a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee24a-103">Очистка списка ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee24a-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee24a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee24a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee24a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee24a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee24a-106">Командлет **Remove-AzureRmDataLakeStoreItemAcl** удаляет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee24a-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ee24a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee24a-107">EXAMPLES</span></span>

### <span data-ttu-id="ee24a-108">Пример 1: Удаление списка ACL из папки</span><span class="sxs-lookup"><span data-stu-id="ee24a-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="ee24a-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ee24a-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="ee24a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee24a-110">PARAMETERS</span></span>

### <span data-ttu-id="ee24a-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ee24a-111">-Account</span></span>
<span data-ttu-id="ee24a-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ee24a-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="ee24a-113">-Default</span><span class="sxs-lookup"><span data-stu-id="ee24a-113">-Default</span></span>
<span data-ttu-id="ee24a-114">Указывает на то, что командлет удаляет список ACL по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="ee24a-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee24a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee24a-115">-DefaultProfile</span></span>
<span data-ttu-id="ee24a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee24a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee24a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ee24a-117">-Force</span></span>
<span data-ttu-id="ee24a-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee24a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee24a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee24a-119">-PassThru</span></span>
<span data-ttu-id="ee24a-120">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="ee24a-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ee24a-121">-Path</span><span class="sxs-lookup"><span data-stu-id="ee24a-121">-Path</span></span>
<span data-ttu-id="ee24a-122">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="ee24a-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ee24a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee24a-123">-Confirm</span></span>
<span data-ttu-id="ee24a-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee24a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee24a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee24a-125">-WhatIf</span></span>
<span data-ttu-id="ee24a-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee24a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee24a-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee24a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee24a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee24a-128">CommonParameters</span></span>
<span data-ttu-id="ee24a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee24a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee24a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee24a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee24a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee24a-131">INPUTS</span></span>

### <span data-ttu-id="ee24a-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="ee24a-132">None</span></span>
<span data-ttu-id="ee24a-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ee24a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee24a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee24a-134">OUTPUTS</span></span>

### <span data-ttu-id="ee24a-135">логических</span><span class="sxs-lookup"><span data-stu-id="ee24a-135">bool</span></span>
<span data-ttu-id="ee24a-136">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="ee24a-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="ee24a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee24a-137">NOTES</span></span>
* <span data-ttu-id="ee24a-138">Alias (псевдоним): Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="ee24a-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="ee24a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee24a-139">RELATED LINKS</span></span>

[<span data-ttu-id="ee24a-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ee24a-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="ee24a-141">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ee24a-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="ee24a-142">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ee24a-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


