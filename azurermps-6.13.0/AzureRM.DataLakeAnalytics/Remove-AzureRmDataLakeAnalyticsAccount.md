---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a04295bca6c664e583ae9653b1f3ed7d52aebf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733865"
---
# <span data-ttu-id="513e0-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="513e0-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="513e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="513e0-102">SYNOPSIS</span></span>
<span data-ttu-id="513e0-103">Удаление учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="513e0-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="513e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="513e0-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="513e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="513e0-105">DESCRIPTION</span></span>
<span data-ttu-id="513e0-106">Командлет **Remove-AzureRmDataLakeAnalyticsAccount** окончательно удаляет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="513e0-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="513e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="513e0-107">EXAMPLES</span></span>

### <span data-ttu-id="513e0-108">Пример 1: Удаление учетной записи</span><span class="sxs-lookup"><span data-stu-id="513e0-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="513e0-109">Эта команда удаляет указанную учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="513e0-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="513e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="513e0-110">PARAMETERS</span></span>

### <span data-ttu-id="513e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513e0-111">-DefaultProfile</span></span>
<span data-ttu-id="513e0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="513e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="513e0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="513e0-113">-Force</span></span>
<span data-ttu-id="513e0-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="513e0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="513e0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="513e0-115">-Name</span></span>
<span data-ttu-id="513e0-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="513e0-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="513e0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="513e0-117">-PassThru</span></span>
<span data-ttu-id="513e0-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="513e0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="513e0-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="513e0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="513e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="513e0-121">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="513e0-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="513e0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="513e0-122">-Confirm</span></span>
<span data-ttu-id="513e0-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="513e0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513e0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513e0-124">-WhatIf</span></span>
<span data-ttu-id="513e0-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="513e0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513e0-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="513e0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513e0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513e0-127">CommonParameters</span></span>
<span data-ttu-id="513e0-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="513e0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513e0-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513e0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513e0-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="513e0-130">INPUTS</span></span>

### <span data-ttu-id="513e0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="513e0-131">System.String</span></span>

## <span data-ttu-id="513e0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="513e0-132">OUTPUTS</span></span>

### <span data-ttu-id="513e0-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="513e0-133">System.Boolean</span></span>

## <span data-ttu-id="513e0-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="513e0-134">NOTES</span></span>

## <span data-ttu-id="513e0-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="513e0-135">RELATED LINKS</span></span>

[<span data-ttu-id="513e0-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="513e0-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="513e0-137">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="513e0-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="513e0-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="513e0-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="513e0-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="513e0-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


