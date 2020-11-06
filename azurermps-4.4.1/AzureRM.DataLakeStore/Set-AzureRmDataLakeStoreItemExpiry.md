---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570420"
---
# <span data-ttu-id="6e1e3-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6e1e3-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="6e1e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1e3-103">Задает или удаляет время окончания срока действия файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e1e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e1e3-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e1e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e1e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1e3-106">Командлет **Set-AzureRmDataLakeStoreItemExpiry** задает или удаляет время окончания для файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6e1e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e1e3-107">EXAMPLES</span></span>

### <span data-ttu-id="6e1e3-108">Пример 1: Установка срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="6e1e3-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="6e1e3-109">Задает срок действия файла в myfile.txt учетной записи в ContosoADL в два часа.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="6e1e3-110">Это приведет к истечении срока действия файла (помечается для удаления) в два часа.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="6e1e3-111">Пример 2: удаление срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="6e1e3-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="6e1e3-112">Удаление срока действия, установленного ранее, для файла "myfile.txt" в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="6e1e3-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="6e1e3-113">Это означает, что срок действия файла не истечет автоматически (помечать для удаления), и его необходимо будет удалить вручную или установить срок действия.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="6e1e3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e1e3-114">PARAMETERS</span></span>

### <span data-ttu-id="6e1e3-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6e1e3-115">-Account</span></span>
<span data-ttu-id="6e1e3-116">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6e1e3-117">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="6e1e3-117">-Expiration</span></span>
<span data-ttu-id="6e1e3-118">Абсолютное время окончания срока действия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="6e1e3-119">Если значение не указано или равно MaxValue, срок действия файла не ограничен.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e3-120">-Path</span><span class="sxs-lookup"><span data-stu-id="6e1e3-120">-Path</span></span>
<span data-ttu-id="6e1e3-121">Задает путь к файлу Data Lake Store для элемента, для которого нужно задать или удалить срок действия.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="6e1e3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e1e3-122">-Confirm</span></span>
<span data-ttu-id="6e1e3-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1e3-124">-WhatIf</span></span>
<span data-ttu-id="6e1e3-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e1e3-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e1e3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1e3-127">-DefaultProfile</span></span>
<span data-ttu-id="6e1e3-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e1e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1e3-129">CommonParameters</span></span>
<span data-ttu-id="6e1e3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1e3-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e1e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1e3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e1e3-132">INPUTS</span></span>

## <span data-ttu-id="6e1e3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e1e3-133">OUTPUTS</span></span>

### <span data-ttu-id="6e1e3-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e1e3-134">DataLakeStoreItem</span></span>
<span data-ttu-id="6e1e3-135">Обновленный файл с новым временем истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="6e1e3-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="6e1e3-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e1e3-136">NOTES</span></span>
<span data-ttu-id="6e1e3-137">Alias (псевдоним): Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6e1e3-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="6e1e3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e1e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e1e3-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e1e3-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

