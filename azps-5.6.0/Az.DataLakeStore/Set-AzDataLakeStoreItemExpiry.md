---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 7dd1fb194ebd14694b15914bdc9d633bb2973b20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995627"
---
# <span data-ttu-id="6b0ef-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6b0ef-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="6b0ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0ef-103">Задает или удаляет срок действия файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6b0ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b0ef-104">SYNTAX</span></span>

### <span data-ttu-id="6b0ef-105">SetAbsoluteNeverExpireExpiry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b0ef-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b0ef-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="6b0ef-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b0ef-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b0ef-107">DESCRIPTION</span></span>
<span data-ttu-id="6b0ef-108">Наборы **cmdletлетов Set-AzDataLakeStoreItemExpiry** либо удаляют время истечения срока действия для файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6b0ef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b0ef-109">EXAMPLES</span></span>

### <span data-ttu-id="6b0ef-110">Пример 1. Настройка срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="6b0ef-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="6b0ef-111">Срок действия myfile.txt в учетной записи ContosoADL истекает через два часа.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="6b0ef-112">В этом случае срок действия файла истечет (будет помечен для удаления) через два часа.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="6b0ef-113">Пример 2. Удаление срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="6b0ef-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="6b0ef-114">Удаляет все сроки действия, задав для файла "myfile.txt" в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="6b0ef-115">Это означает, что срок действия файла не истечет автоматически (он будет помечен для удаления) и потребуется удалить его вручную или установить срок действия еще раз.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="6b0ef-116">Пример 3. Установите время окончания срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="6b0ef-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="6b0ef-117">Первая команда задает время окончания срока действия файла /myfile.txt 240 секунд относительно текущего времени на сервере.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="6b0ef-118">Вторая команда задает время окончания срока действия файла /myfile.txt 240 секунд относительно времени создания на сервере.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="6b0ef-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b0ef-119">PARAMETERS</span></span>

### <span data-ttu-id="6b0ef-120">-Account</span><span class="sxs-lookup"><span data-stu-id="6b0ef-120">-Account</span></span>
<span data-ttu-id="6b0ef-121">Указывает имя учетной записи Магазина данных.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6b0ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0ef-122">-DefaultProfile</span></span>
<span data-ttu-id="6b0ef-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b0ef-124">-Expiration</span><span class="sxs-lookup"><span data-stu-id="6b0ef-124">-Expiration</span></span>
<span data-ttu-id="6b0ef-125">Абсолютный срок действия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="6b0ef-126">Если значение или значение MaxValue не установлено, срок действия файла не истечет.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="6b0ef-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6b0ef-127">-Path</span></span>
<span data-ttu-id="6b0ef-128">Путь к файлу, для которого нужно установить или удалить срок действия.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="6b0ef-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="6b0ef-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="6b0ef-130">Относительные варианты срока действия.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-130">Relative expiry options.</span></span> <span data-ttu-id="6b0ef-131">RelativeToNow или RelativeToCreationDate — это текущие параметры</span><span class="sxs-lookup"><span data-stu-id="6b0ef-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="6b0ef-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="6b0ef-132">-RelativeTime</span></span>
<span data-ttu-id="6b0ef-133">Относительное время в миллисекунах относительно времени создания или времени создания.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="6b0ef-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b0ef-134">-Confirm</span></span>
<span data-ttu-id="6b0ef-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b0ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b0ef-136">-WhatIf</span></span>
<span data-ttu-id="6b0ef-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b0ef-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b0ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0ef-139">CommonParameters</span></span>
<span data-ttu-id="6b0ef-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0ef-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b0ef-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0ef-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0ef-142">INPUTS</span></span>

### <span data-ttu-id="6b0ef-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6b0ef-143">System.String</span></span>

### <span data-ttu-id="6b0ef-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6b0ef-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6b0ef-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6b0ef-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="6b0ef-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="6b0ef-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="6b0ef-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="6b0ef-147">System.Int64</span></span>

## <span data-ttu-id="6b0ef-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b0ef-148">OUTPUTS</span></span>

### <span data-ttu-id="6b0ef-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b0ef-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="6b0ef-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b0ef-150">NOTES</span></span>
<span data-ttu-id="6b0ef-151">Псевдоним: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6b0ef-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="6b0ef-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b0ef-152">RELATED LINKS</span></span>

[<span data-ttu-id="6b0ef-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b0ef-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

