---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243651"
---
# <span data-ttu-id="8e475-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="8e475-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="8e475-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e475-102">SYNOPSIS</span></span>
<span data-ttu-id="8e475-103">Задает или удаляет время окончания срока действия файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8e475-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="8e475-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e475-104">SYNTAX</span></span>

### <span data-ttu-id="8e475-105">SetAbsoluteNeverExpireExpiry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e475-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e475-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="8e475-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e475-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e475-107">DESCRIPTION</span></span>
<span data-ttu-id="8e475-108">Командлет **Set-AzDataLakeStoreItemExpiry** задает или удаляет время окончания для файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8e475-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="8e475-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e475-109">EXAMPLES</span></span>

### <span data-ttu-id="8e475-110">Пример 1: Установка срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="8e475-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="8e475-111">Задает срок действия файла в myfile.txt учетной записи в ContosoADL в два часа.</span><span class="sxs-lookup"><span data-stu-id="8e475-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="8e475-112">Это приведет к истечении срока действия файла (помечается для удаления) в два часа.</span><span class="sxs-lookup"><span data-stu-id="8e475-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="8e475-113">Пример 2: удаление срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="8e475-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="8e475-114">Удаление срока действия, установленного ранее, для файла "myfile.txt" в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="8e475-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="8e475-115">Это означает, что срок действия файла не истечет автоматически (помечать для удаления), и его необходимо будет удалить вручную или установить срок действия.</span><span class="sxs-lookup"><span data-stu-id="8e475-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="8e475-116">Пример 3: Настройка срока действия файла относительно текущего времени</span><span class="sxs-lookup"><span data-stu-id="8e475-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="8e475-117">Первая команда задает время истечения срока действия файла/myfile.txt 240 секунды относительно текущего времени на сервере.</span><span class="sxs-lookup"><span data-stu-id="8e475-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="8e475-118">Вторая команда задает время истечения срока действия файла/myfile.txt 240 секунд относительно времени создания на сервере.</span><span class="sxs-lookup"><span data-stu-id="8e475-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="8e475-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e475-119">PARAMETERS</span></span>

### <span data-ttu-id="8e475-120">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8e475-120">-Account</span></span>
<span data-ttu-id="8e475-121">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8e475-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="8e475-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e475-122">-DefaultProfile</span></span>
<span data-ttu-id="8e475-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e475-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e475-124">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="8e475-124">-Expiration</span></span>
<span data-ttu-id="8e475-125">Абсолютное время окончания срока действия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="8e475-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="8e475-126">Если значение не указано или равно MaxValue, срок действия файла не ограничен.</span><span class="sxs-lookup"><span data-stu-id="8e475-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e475-127">-Path</span><span class="sxs-lookup"><span data-stu-id="8e475-127">-Path</span></span>
<span data-ttu-id="8e475-128">Задает путь к файлу Data Lake Store для элемента, для которого нужно задать или удалить срок действия.</span><span class="sxs-lookup"><span data-stu-id="8e475-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="8e475-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="8e475-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="8e475-130">Относительные параметры срока действия.</span><span class="sxs-lookup"><span data-stu-id="8e475-130">Relative expiry options.</span></span> <span data-ttu-id="8e475-131">RelativeToNow или RelativeToCreationDate являются текущими параметрами</span><span class="sxs-lookup"><span data-stu-id="8e475-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e475-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="8e475-132">-RelativeTime</span></span>
<span data-ttu-id="8e475-133">Относительное время (в миллисекундах), по отношению к моменту и времени создания</span><span class="sxs-lookup"><span data-stu-id="8e475-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e475-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e475-134">-Confirm</span></span>
<span data-ttu-id="8e475-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e475-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e475-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e475-136">-WhatIf</span></span>
<span data-ttu-id="8e475-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e475-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e475-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e475-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e475-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e475-139">CommonParameters</span></span>
<span data-ttu-id="8e475-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e475-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e475-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e475-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e475-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e475-142">INPUTS</span></span>

### <span data-ttu-id="8e475-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8e475-143">System.String</span></span>

### <span data-ttu-id="8e475-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8e475-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8e475-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8e475-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="8e475-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="8e475-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="8e475-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="8e475-147">System.Int64</span></span>

## <span data-ttu-id="8e475-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e475-148">OUTPUTS</span></span>

### <span data-ttu-id="8e475-149">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8e475-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="8e475-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e475-150">NOTES</span></span>
<span data-ttu-id="8e475-151">Alias (псевдоним): Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="8e475-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="8e475-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e475-152">RELATED LINKS</span></span>

[<span data-ttu-id="8e475-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8e475-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

