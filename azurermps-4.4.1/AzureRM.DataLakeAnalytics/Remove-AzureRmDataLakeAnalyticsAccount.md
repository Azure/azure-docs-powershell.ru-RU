---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559856"
---
# <span data-ttu-id="ffc08-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ffc08-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="ffc08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffc08-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc08-103">Удаление учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc08-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffc08-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffc08-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc08-106">Командлет **Remove-AzureRmDataLakeAnalyticsAccount** окончательно удаляет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc08-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ffc08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffc08-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc08-108">Пример 1: Удаление учетной записи</span><span class="sxs-lookup"><span data-stu-id="ffc08-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="ffc08-109">Эта команда удаляет указанную учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc08-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="ffc08-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffc08-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc08-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ffc08-111">-Force</span></span>
<span data-ttu-id="ffc08-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ffc08-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc08-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffc08-113">-Name</span></span>
<span data-ttu-id="ffc08-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc08-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc08-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffc08-115">-PassThru</span></span>
<span data-ttu-id="ffc08-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ffc08-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ffc08-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ffc08-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc08-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc08-118">-ResourceGroupName</span></span>
<span data-ttu-id="ffc08-119">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc08-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc08-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc08-120">-Confirm</span></span>
<span data-ttu-id="ffc08-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffc08-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc08-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc08-122">-WhatIf</span></span>
<span data-ttu-id="ffc08-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffc08-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc08-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffc08-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc08-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc08-125">-DefaultProfile</span></span>
<span data-ttu-id="ffc08-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc08-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc08-127">CommonParameters</span></span>
<span data-ttu-id="ffc08-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffc08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc08-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc08-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc08-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffc08-130">INPUTS</span></span>

## <span data-ttu-id="ffc08-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffc08-131">OUTPUTS</span></span>

### <span data-ttu-id="ffc08-132">логических</span><span class="sxs-lookup"><span data-stu-id="ffc08-132">bool</span></span>
<span data-ttu-id="ffc08-133">Если указана функция PassThru, возвращает значение истина после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="ffc08-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="ffc08-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffc08-134">NOTES</span></span>

## <span data-ttu-id="ffc08-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffc08-135">RELATED LINKS</span></span>

[<span data-ttu-id="ffc08-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ffc08-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ffc08-137">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ffc08-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ffc08-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ffc08-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="ffc08-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="ffc08-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


