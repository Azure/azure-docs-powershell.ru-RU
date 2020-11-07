---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9339857a125ca0646869a81749f9cf55ff2531ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731059"
---
# <span data-ttu-id="577c0-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="577c0-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="577c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="577c0-102">SYNOPSIS</span></span>
<span data-ttu-id="577c0-103">Очистка списка ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="577c0-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="577c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="577c0-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="577c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="577c0-105">DESCRIPTION</span></span>
<span data-ttu-id="577c0-106">Командлет **Remove-AzDataLakeStoreItemAcl** удаляет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="577c0-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="577c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="577c0-107">EXAMPLES</span></span>

### <span data-ttu-id="577c0-108">Пример 1: Удаление списка ACL из папки</span><span class="sxs-lookup"><span data-stu-id="577c0-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="577c0-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="577c0-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="577c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="577c0-110">PARAMETERS</span></span>

### <span data-ttu-id="577c0-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="577c0-111">-Account</span></span>
<span data-ttu-id="577c0-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="577c0-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="577c0-113">-Default</span><span class="sxs-lookup"><span data-stu-id="577c0-113">-Default</span></span>
<span data-ttu-id="577c0-114">Указывает на то, что командлет удаляет список ACL по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="577c0-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577c0-115">-DefaultProfile</span></span>
<span data-ttu-id="577c0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="577c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="577c0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="577c0-117">-Force</span></span>
<span data-ttu-id="577c0-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="577c0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="577c0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="577c0-119">-PassThru</span></span>
<span data-ttu-id="577c0-120">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="577c0-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577c0-121">-Path</span><span class="sxs-lookup"><span data-stu-id="577c0-121">-Path</span></span>
<span data-ttu-id="577c0-122">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="577c0-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="577c0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="577c0-123">-Confirm</span></span>
<span data-ttu-id="577c0-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="577c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577c0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577c0-125">-WhatIf</span></span>
<span data-ttu-id="577c0-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="577c0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577c0-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="577c0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577c0-128">CommonParameters</span></span>
<span data-ttu-id="577c0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="577c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577c0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577c0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577c0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="577c0-131">INPUTS</span></span>

### <span data-ttu-id="577c0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="577c0-132">System.String</span></span>

### <span data-ttu-id="577c0-133">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="577c0-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="577c0-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="577c0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="577c0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="577c0-135">OUTPUTS</span></span>

### <span data-ttu-id="577c0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="577c0-136">System.Boolean</span></span>

## <span data-ttu-id="577c0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="577c0-137">NOTES</span></span>
* <span data-ttu-id="577c0-138">Alias (псевдоним): Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="577c0-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="577c0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="577c0-139">RELATED LINKS</span></span>

[<span data-ttu-id="577c0-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="577c0-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="577c0-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="577c0-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="577c0-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="577c0-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


