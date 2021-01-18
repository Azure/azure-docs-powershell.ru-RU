---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504625"
---
# <span data-ttu-id="4d973-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4d973-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4d973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d973-102">SYNOPSIS</span></span>
<span data-ttu-id="4d973-103">Удаляет учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d973-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4d973-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d973-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d973-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d973-105">DESCRIPTION</span></span>
<span data-ttu-id="4d973-106">**Cmdlet Remove-AzDataLakeAnalyticsAccount** окончательно удаляет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d973-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4d973-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d973-107">EXAMPLES</span></span>

### <span data-ttu-id="4d973-108">Пример 1. Удаление учетной записи</span><span class="sxs-lookup"><span data-stu-id="4d973-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="4d973-109">Эта команда удаляет указанную учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d973-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="4d973-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d973-110">PARAMETERS</span></span>

### <span data-ttu-id="4d973-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d973-111">-DefaultProfile</span></span>
<span data-ttu-id="4d973-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d973-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d973-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4d973-113">-Force</span></span>
<span data-ttu-id="4d973-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4d973-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d973-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d973-115">-Name</span></span>
<span data-ttu-id="4d973-116">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d973-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4d973-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d973-117">-PassThru</span></span>
<span data-ttu-id="4d973-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4d973-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d973-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4d973-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d973-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d973-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d973-121">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d973-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="4d973-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d973-122">-Confirm</span></span>
<span data-ttu-id="4d973-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d973-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d973-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d973-124">-WhatIf</span></span>
<span data-ttu-id="4d973-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d973-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d973-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d973-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d973-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d973-127">CommonParameters</span></span>
<span data-ttu-id="4d973-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d973-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d973-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d973-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d973-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d973-130">INPUTS</span></span>

### <span data-ttu-id="4d973-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4d973-131">System.String</span></span>

## <span data-ttu-id="4d973-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d973-132">OUTPUTS</span></span>

### <span data-ttu-id="4d973-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d973-133">System.Boolean</span></span>

## <span data-ttu-id="4d973-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d973-134">NOTES</span></span>

## <span data-ttu-id="4d973-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d973-135">RELATED LINKS</span></span>

[<span data-ttu-id="4d973-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4d973-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4d973-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4d973-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4d973-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4d973-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4d973-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4d973-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


