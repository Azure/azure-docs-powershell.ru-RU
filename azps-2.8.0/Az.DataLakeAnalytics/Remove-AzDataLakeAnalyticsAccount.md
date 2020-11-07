---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721376"
---
# <span data-ttu-id="c1fda-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1fda-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="c1fda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1fda-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fda-103">Удаление учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1fda-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c1fda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1fda-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1fda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1fda-105">DESCRIPTION</span></span>
<span data-ttu-id="c1fda-106">Командлет **Remove-AzDataLakeAnalyticsAccount** окончательно удаляет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1fda-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c1fda-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1fda-107">EXAMPLES</span></span>

### <span data-ttu-id="c1fda-108">Пример 1: Удаление учетной записи</span><span class="sxs-lookup"><span data-stu-id="c1fda-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="c1fda-109">Эта команда удаляет указанную учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1fda-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="c1fda-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1fda-110">PARAMETERS</span></span>

### <span data-ttu-id="c1fda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fda-111">-DefaultProfile</span></span>
<span data-ttu-id="c1fda-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c1fda-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1fda-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c1fda-113">-Force</span></span>
<span data-ttu-id="c1fda-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1fda-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1fda-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1fda-115">-Name</span></span>
<span data-ttu-id="c1fda-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1fda-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c1fda-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1fda-117">-PassThru</span></span>
<span data-ttu-id="c1fda-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c1fda-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1fda-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c1fda-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1fda-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fda-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1fda-121">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c1fda-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="c1fda-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1fda-122">-Confirm</span></span>
<span data-ttu-id="c1fda-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1fda-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1fda-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1fda-124">-WhatIf</span></span>
<span data-ttu-id="c1fda-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1fda-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1fda-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1fda-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1fda-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fda-127">CommonParameters</span></span>
<span data-ttu-id="c1fda-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1fda-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fda-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fda-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fda-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1fda-130">INPUTS</span></span>

### <span data-ttu-id="c1fda-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c1fda-131">System.String</span></span>

## <span data-ttu-id="c1fda-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1fda-132">OUTPUTS</span></span>

### <span data-ttu-id="c1fda-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fda-133">System.Boolean</span></span>

## <span data-ttu-id="c1fda-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1fda-134">NOTES</span></span>

## <span data-ttu-id="c1fda-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1fda-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1fda-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1fda-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1fda-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1fda-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1fda-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1fda-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="c1fda-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="c1fda-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


