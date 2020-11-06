---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 48edcb93cb8fce66c9175bdcf498bd6545949090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566738"
---
# <span data-ttu-id="c5dd9-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c5dd9-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="c5dd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5dd9-103">Очистка списка ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5dd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5dd9-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5dd9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="c5dd9-106">Командлет **Remove-AzureRmDataLakeStoreItemAcl** удаляет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c5dd9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="c5dd9-108">Пример 1: Удаление списка ACL из папки</span><span class="sxs-lookup"><span data-stu-id="c5dd9-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="c5dd9-109">Эта команда удаляет ACL для корневого каталога учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="c5dd9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5dd9-110">PARAMETERS</span></span>

### <span data-ttu-id="c5dd9-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c5dd9-111">-Account</span></span>
<span data-ttu-id="c5dd9-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="c5dd9-113">-Default</span><span class="sxs-lookup"><span data-stu-id="c5dd9-113">-Default</span></span>
<span data-ttu-id="c5dd9-114">Указывает на то, что командлет удаляет список ACL по умолчанию для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="c5dd9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c5dd9-115">-Force</span></span>
<span data-ttu-id="c5dd9-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5dd9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5dd9-117">-PassThru</span></span>
<span data-ttu-id="c5dd9-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="c5dd9-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c5dd9-119">-Path</span></span>
<span data-ttu-id="c5dd9-120">Указывает путь к Data Lake Store для элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c5dd9-120">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c5dd9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5dd9-121">-Confirm</span></span>
<span data-ttu-id="c5dd9-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5dd9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5dd9-123">-WhatIf</span></span>
<span data-ttu-id="c5dd9-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5dd9-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5dd9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5dd9-126">-DefaultProfile</span></span>
<span data-ttu-id="c5dd9-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5dd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5dd9-128">CommonParameters</span></span>
<span data-ttu-id="c5dd9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5dd9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5dd9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5dd9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5dd9-131">INPUTS</span></span>

## <span data-ttu-id="c5dd9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5dd9-132">OUTPUTS</span></span>

### <span data-ttu-id="c5dd9-133">логических</span><span class="sxs-lookup"><span data-stu-id="c5dd9-133">bool</span></span>
<span data-ttu-id="c5dd9-134">Если указана функция PassThru, при успешном завершении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="c5dd9-134">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="c5dd9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5dd9-135">NOTES</span></span>
* <span data-ttu-id="c5dd9-136">Alias (псевдоним): Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="c5dd9-136">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="c5dd9-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5dd9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c5dd9-138">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c5dd9-138">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="c5dd9-139">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c5dd9-139">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="c5dd9-140">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c5dd9-140">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


