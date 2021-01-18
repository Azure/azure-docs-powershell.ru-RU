---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: ed7b1a0c0c969f2593d045549f897a172a88f6aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504566"
---
# <span data-ttu-id="5a291-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="5a291-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="5a291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a291-102">SYNOPSIS</span></span>
<span data-ttu-id="5a291-103">Очищает ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5a291-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5a291-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a291-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a291-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a291-105">DESCRIPTION</span></span>
<span data-ttu-id="5a291-106">При наложении на файл или папку из магазина Data Lake Store список управления доступом удаляется с учетом списка контроля доступа **(Remove-AzDataLakeStoreItemAcl).**</span><span class="sxs-lookup"><span data-stu-id="5a291-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5a291-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a291-107">EXAMPLES</span></span>

### <span data-ttu-id="5a291-108">Пример 1. Удаление ACL из папки</span><span class="sxs-lookup"><span data-stu-id="5a291-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="5a291-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="5a291-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="5a291-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a291-110">PARAMETERS</span></span>

### <span data-ttu-id="5a291-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5a291-111">-Account</span></span>
<span data-ttu-id="5a291-112">Указывает имя учетной записи Магазина данных.</span><span class="sxs-lookup"><span data-stu-id="5a291-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="5a291-113">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a291-113">-Default</span></span>
<span data-ttu-id="5a291-114">Указывает на то, что этот cmdlet удаляет значение ACL по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="5a291-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="5a291-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a291-115">-DefaultProfile</span></span>
<span data-ttu-id="5a291-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a291-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a291-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a291-117">-Force</span></span>
<span data-ttu-id="5a291-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5a291-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a291-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a291-119">-PassThru</span></span>
<span data-ttu-id="5a291-120">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="5a291-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="5a291-121">-Path</span><span class="sxs-lookup"><span data-stu-id="5a291-121">-Path</span></span>
<span data-ttu-id="5a291-122">Путь к элементу в Магазине данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="5a291-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5a291-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a291-123">-Confirm</span></span>
<span data-ttu-id="5a291-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a291-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a291-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a291-125">-WhatIf</span></span>
<span data-ttu-id="5a291-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a291-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a291-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a291-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a291-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a291-128">CommonParameters</span></span>
<span data-ttu-id="5a291-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a291-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a291-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a291-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a291-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a291-131">INPUTS</span></span>

### <span data-ttu-id="5a291-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5a291-132">System.String</span></span>

### <span data-ttu-id="5a291-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5a291-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5a291-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a291-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a291-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a291-135">OUTPUTS</span></span>

### <span data-ttu-id="5a291-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a291-136">System.Boolean</span></span>

## <span data-ttu-id="5a291-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a291-137">NOTES</span></span>
* <span data-ttu-id="5a291-138">Псевдоним: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="5a291-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="5a291-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a291-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a291-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a291-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="5a291-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="5a291-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="5a291-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a291-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


