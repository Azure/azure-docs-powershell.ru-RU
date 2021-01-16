---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400647"
---
# <span data-ttu-id="2d516-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2d516-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="2d516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d516-102">SYNOPSIS</span></span>
<span data-ttu-id="2d516-103">Очищает ACL файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d516-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2d516-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d516-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d516-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d516-105">DESCRIPTION</span></span>
<span data-ttu-id="2d516-106">При наложении cmdlet **Remove-AzDataLakeStoreItemAcl** список управления доступом очищается из списка управления доступом файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d516-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2d516-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d516-107">EXAMPLES</span></span>

### <span data-ttu-id="2d516-108">Пример 1. Удаление ACL из папки</span><span class="sxs-lookup"><span data-stu-id="2d516-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="2d516-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="2d516-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="2d516-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d516-110">PARAMETERS</span></span>

### <span data-ttu-id="2d516-111">-Account</span><span class="sxs-lookup"><span data-stu-id="2d516-111">-Account</span></span>
<span data-ttu-id="2d516-112">Указывает имя учетной записи Для магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d516-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="2d516-113">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2d516-113">-Default</span></span>
<span data-ttu-id="2d516-114">Указывает на то, что по умолчанию удаляется значение ACL, задаваемая по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="2d516-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="2d516-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d516-115">-DefaultProfile</span></span>
<span data-ttu-id="2d516-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d516-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d516-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d516-117">-Force</span></span>
<span data-ttu-id="2d516-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2d516-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d516-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d516-119">-PassThru</span></span>
<span data-ttu-id="2d516-120">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="2d516-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="2d516-121">-Path</span><span class="sxs-lookup"><span data-stu-id="2d516-121">-Path</span></span>
<span data-ttu-id="2d516-122">Путь к элементу в Магазине данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="2d516-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2d516-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d516-123">-Confirm</span></span>
<span data-ttu-id="2d516-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2d516-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d516-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d516-125">-WhatIf</span></span>
<span data-ttu-id="2d516-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d516-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d516-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d516-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d516-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d516-128">CommonParameters</span></span>
<span data-ttu-id="2d516-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d516-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d516-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d516-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d516-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d516-131">INPUTS</span></span>

### <span data-ttu-id="2d516-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2d516-132">System.String</span></span>

### <span data-ttu-id="2d516-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2d516-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2d516-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d516-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d516-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d516-135">OUTPUTS</span></span>

### <span data-ttu-id="2d516-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d516-136">System.Boolean</span></span>

## <span data-ttu-id="2d516-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d516-137">NOTES</span></span>
* <span data-ttu-id="2d516-138">Псевдоним: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="2d516-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="2d516-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d516-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d516-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d516-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="2d516-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2d516-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="2d516-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d516-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


