---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065525"
---
# <span data-ttu-id="f4d78-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f4d78-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="f4d78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4d78-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d78-103">Очистка списка ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4d78-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f4d78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4d78-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4d78-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d78-106">Командлет **Remove-AzDataLakeStoreItemAcl** удаляет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4d78-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f4d78-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4d78-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d78-108">Пример 1: Удаление списка ACL из папки</span><span class="sxs-lookup"><span data-stu-id="f4d78-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="f4d78-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="f4d78-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="f4d78-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4d78-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d78-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f4d78-111">-Account</span></span>
<span data-ttu-id="f4d78-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4d78-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="f4d78-113">-Default</span><span class="sxs-lookup"><span data-stu-id="f4d78-113">-Default</span></span>
<span data-ttu-id="f4d78-114">Указывает на то, что командлет удаляет список ACL по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="f4d78-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="f4d78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d78-115">-DefaultProfile</span></span>
<span data-ttu-id="f4d78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4d78-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4d78-117">-Force</span></span>
<span data-ttu-id="f4d78-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4d78-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4d78-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4d78-119">-PassThru</span></span>
<span data-ttu-id="f4d78-120">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="f4d78-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="f4d78-121">-Path</span><span class="sxs-lookup"><span data-stu-id="f4d78-121">-Path</span></span>
<span data-ttu-id="f4d78-122">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="f4d78-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f4d78-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4d78-123">-Confirm</span></span>
<span data-ttu-id="f4d78-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4d78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d78-125">-WhatIf</span></span>
<span data-ttu-id="f4d78-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4d78-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d78-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4d78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d78-128">CommonParameters</span></span>
<span data-ttu-id="f4d78-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4d78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d78-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d78-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d78-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4d78-131">INPUTS</span></span>

### <span data-ttu-id="f4d78-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d78-132">System.String</span></span>

### <span data-ttu-id="f4d78-133">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f4d78-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f4d78-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4d78-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4d78-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4d78-135">OUTPUTS</span></span>

### <span data-ttu-id="f4d78-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4d78-136">System.Boolean</span></span>

## <span data-ttu-id="f4d78-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4d78-137">NOTES</span></span>
* <span data-ttu-id="f4d78-138">Alias (псевдоним): Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="f4d78-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="f4d78-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4d78-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4d78-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f4d78-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="f4d78-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="f4d78-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="f4d78-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f4d78-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


