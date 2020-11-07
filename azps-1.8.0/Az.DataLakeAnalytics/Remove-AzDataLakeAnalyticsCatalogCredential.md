---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 79e5823c797c878643ea6ad2870873da363d0312
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731089"
---
# <span data-ttu-id="60e0f-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="60e0f-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="60e0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="60e0f-103">Удаление учетных данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60e0f-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="60e0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60e0f-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="60e0f-106">Командлет Remove-AzDataLakeAnalyticsCatalogCredential удаляет учетные данные каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60e0f-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="60e0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60e0f-107">EXAMPLES</span></span>

### <span data-ttu-id="60e0f-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="60e0f-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="60e0f-109">Эта команда удаляет указанные учетные данные для каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60e0f-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="60e0f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60e0f-110">PARAMETERS</span></span>

### <span data-ttu-id="60e0f-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="60e0f-111">-Account</span></span>
<span data-ttu-id="60e0f-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="60e0f-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="60e0f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60e0f-113">-DatabaseName</span></span>
<span data-ttu-id="60e0f-114">Указывает имя базы данных, в которой хранятся учетные данные.</span><span class="sxs-lookup"><span data-stu-id="60e0f-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e0f-115">-DefaultProfile</span></span>
<span data-ttu-id="60e0f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="60e0f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60e0f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60e0f-117">-Force</span></span>
<span data-ttu-id="60e0f-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="60e0f-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e0f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60e0f-119">-Name</span></span>
<span data-ttu-id="60e0f-120">Указывает имя учетных данных.</span><span class="sxs-lookup"><span data-stu-id="60e0f-120">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e0f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60e0f-121">-PassThru</span></span>
<span data-ttu-id="60e0f-122">Указывает на то, что этот командлет не ждет завершения операции.</span><span class="sxs-lookup"><span data-stu-id="60e0f-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="60e0f-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="60e0f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60e0f-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="60e0f-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e0f-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="60e0f-125">-Password</span></span>
<span data-ttu-id="60e0f-126">Пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="60e0f-126">The password for the credential.</span></span>
<span data-ttu-id="60e0f-127">Это необходимо, если вызывающий абонент не является владельцем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="60e0f-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e0f-128">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="60e0f-128">-Recurse</span></span>
<span data-ttu-id="60e0f-129">Указывает на то, что эта операция удаления должна пройти и удалить все ресурсы, зависящие от этих учетных данных, а также удалять их.</span><span class="sxs-lookup"><span data-stu-id="60e0f-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="60e0f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60e0f-130">-Confirm</span></span>
<span data-ttu-id="60e0f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60e0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e0f-132">-WhatIf</span></span>
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

### <span data-ttu-id="60e0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e0f-133">CommonParameters</span></span>
<span data-ttu-id="60e0f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60e0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e0f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e0f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e0f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60e0f-136">INPUTS</span></span>

### <span data-ttu-id="60e0f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="60e0f-137">System.String</span></span>

### <span data-ttu-id="60e0f-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="60e0f-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="60e0f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60e0f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60e0f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e0f-140">OUTPUTS</span></span>

### <span data-ttu-id="60e0f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60e0f-141">System.Boolean</span></span>

## <span data-ttu-id="60e0f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="60e0f-142">NOTES</span></span>

## <span data-ttu-id="60e0f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60e0f-143">RELATED LINKS</span></span>
