---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 2ee08eaf9dae9a6d2001608d8ef247c7e116c98e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561839"
---
# <span data-ttu-id="23a01-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="23a01-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="23a01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23a01-102">SYNOPSIS</span></span>
<span data-ttu-id="23a01-103">Удаление секрета Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23a01-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23a01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23a01-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23a01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23a01-105">DESCRIPTION</span></span>
<span data-ttu-id="23a01-106">Командлет **Remove-AzureRmDataLakeAnalyticsCatalogSecret** удаляет секретный ключ для каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23a01-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="23a01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23a01-107">EXAMPLES</span></span>

### <span data-ttu-id="23a01-108">Пример 1: удаление секрета</span><span class="sxs-lookup"><span data-stu-id="23a01-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="23a01-109">Эта команда удаляет секретный код, указанный в каталоге Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23a01-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="23a01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23a01-110">PARAMETERS</span></span>

### <span data-ttu-id="23a01-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="23a01-111">-Account</span></span>
<span data-ttu-id="23a01-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23a01-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="23a01-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23a01-113">-DatabaseName</span></span>
<span data-ttu-id="23a01-114">Указывает имя базы данных, в которой хранится секрет.</span><span class="sxs-lookup"><span data-stu-id="23a01-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a01-115">-DefaultProfile</span></span>
<span data-ttu-id="23a01-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23a01-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23a01-117">-Force</span><span class="sxs-lookup"><span data-stu-id="23a01-117">-Force</span></span>
<span data-ttu-id="23a01-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="23a01-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a01-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23a01-119">-Name</span></span>
<span data-ttu-id="23a01-120">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="23a01-120">Specifies the name of the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a01-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23a01-121">-PassThru</span></span>
<span data-ttu-id="23a01-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="23a01-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23a01-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="23a01-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a01-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23a01-124">-Confirm</span></span>
<span data-ttu-id="23a01-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23a01-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23a01-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a01-126">-WhatIf</span></span>
<span data-ttu-id="23a01-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23a01-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a01-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23a01-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23a01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a01-129">CommonParameters</span></span>
<span data-ttu-id="23a01-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23a01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a01-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a01-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a01-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23a01-132">INPUTS</span></span>

### <span data-ttu-id="23a01-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="23a01-133">None</span></span>
<span data-ttu-id="23a01-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="23a01-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23a01-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23a01-135">OUTPUTS</span></span>

### <span data-ttu-id="23a01-136">логических</span><span class="sxs-lookup"><span data-stu-id="23a01-136">bool</span></span>
<span data-ttu-id="23a01-137">Если указана функция PassThru, возвращает значение истина после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="23a01-137">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="23a01-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="23a01-138">NOTES</span></span>

## <span data-ttu-id="23a01-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23a01-139">RELATED LINKS</span></span>

[<span data-ttu-id="23a01-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="23a01-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="23a01-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="23a01-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


