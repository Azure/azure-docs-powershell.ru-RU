---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734563"
---
# <span data-ttu-id="0fc58-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0fc58-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="0fc58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fc58-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc58-103">Изменение ACL для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0fc58-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fc58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fc58-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fc58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc58-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc58-106">Командлет **Set-AzureRmDataLakeStoreItemAcl** изменяет список управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0fc58-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0fc58-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fc58-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc58-108">Пример 1: Настройка ACL для файла и папки</span><span class="sxs-lookup"><span data-stu-id="0fc58-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="0fc58-109">Первая команда получает ACL для корневого каталога учетной записи ContosoADL и сохраняет ее в переменной $ACL.</span><span class="sxs-lookup"><span data-stu-id="0fc58-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="0fc58-110">Вторая команда задает для списка ACL для файла Test.txt значение, заданное в $ACL.</span><span class="sxs-lookup"><span data-stu-id="0fc58-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="0fc58-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fc58-111">PARAMETERS</span></span>

### <span data-ttu-id="0fc58-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0fc58-112">-Account</span></span>
<span data-ttu-id="0fc58-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0fc58-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0fc58-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="0fc58-114">-Acl</span></span>
<span data-ttu-id="0fc58-115">Указывает список ACL для файла или папки.</span><span class="sxs-lookup"><span data-stu-id="0fc58-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc58-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fc58-116">-PassThru</span></span>
<span data-ttu-id="0fc58-117">Указывает на то, что результирующий список ACL должен возвращаться.</span><span class="sxs-lookup"><span data-stu-id="0fc58-117">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="0fc58-118">-Path</span><span class="sxs-lookup"><span data-stu-id="0fc58-118">-Path</span></span>
<span data-ttu-id="0fc58-119">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="0fc58-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0fc58-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fc58-120">-Confirm</span></span>
<span data-ttu-id="0fc58-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fc58-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc58-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc58-122">-WhatIf</span></span>
<span data-ttu-id="0fc58-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fc58-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc58-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fc58-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc58-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc58-125">-DefaultProfile</span></span>
<span data-ttu-id="0fc58-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc58-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fc58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc58-127">CommonParameters</span></span>
<span data-ttu-id="0fc58-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fc58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc58-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc58-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fc58-130">INPUTS</span></span>

### <span data-ttu-id="0fc58-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="0fc58-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="0fc58-132">Параметр "ACL" принимает значение типа "DataLakeStoreItemAce []" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0fc58-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="0fc58-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc58-133">OUTPUTS</span></span>

### <span data-ttu-id="0fc58-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="0fc58-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="0fc58-135">Если указана проpassthru, будет возвращен результирующий список записей ACL.</span><span class="sxs-lookup"><span data-stu-id="0fc58-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="0fc58-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fc58-136">NOTES</span></span>

## <span data-ttu-id="0fc58-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fc58-137">RELATED LINKS</span></span>

