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
ms.locfileid: "93721374"
---
# <span data-ttu-id="7e70a-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="7e70a-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="7e70a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e70a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e70a-103">Удаление учетных данных Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e70a-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="7e70a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e70a-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e70a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e70a-105">DESCRIPTION</span></span>
<span data-ttu-id="7e70a-106">Командлет Remove-AzDataLakeAnalyticsCatalogCredential удаляет учетные данные каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e70a-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="7e70a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e70a-107">EXAMPLES</span></span>

### <span data-ttu-id="7e70a-108">Пример 1: удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="7e70a-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="7e70a-109">Эта команда удаляет указанные учетные данные для каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e70a-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="7e70a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e70a-110">PARAMETERS</span></span>

### <span data-ttu-id="7e70a-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7e70a-111">-Account</span></span>
<span data-ttu-id="7e70a-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e70a-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7e70a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e70a-113">-DatabaseName</span></span>
<span data-ttu-id="7e70a-114">Указывает имя базы данных, в которой хранятся учетные данные.</span><span class="sxs-lookup"><span data-stu-id="7e70a-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="7e70a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e70a-115">-DefaultProfile</span></span>
<span data-ttu-id="7e70a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e70a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e70a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7e70a-117">-Force</span></span>
<span data-ttu-id="7e70a-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e70a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e70a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e70a-119">-Name</span></span>
<span data-ttu-id="7e70a-120">Указывает имя учетных данных.</span><span class="sxs-lookup"><span data-stu-id="7e70a-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="7e70a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e70a-121">-PassThru</span></span>
<span data-ttu-id="7e70a-122">Указывает на то, что этот командлет не ждет завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7e70a-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="7e70a-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7e70a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e70a-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7e70a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e70a-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="7e70a-125">-Password</span></span>
<span data-ttu-id="7e70a-126">Пароль для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="7e70a-126">The password for the credential.</span></span>
<span data-ttu-id="7e70a-127">Это необходимо, если вызывающий абонент не является владельцем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7e70a-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="7e70a-128">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="7e70a-128">-Recurse</span></span>
<span data-ttu-id="7e70a-129">Указывает на то, что эта операция удаления должна пройти и удалить все ресурсы, зависящие от этих учетных данных, а также удалять их.</span><span class="sxs-lookup"><span data-stu-id="7e70a-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="7e70a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e70a-130">-Confirm</span></span>
<span data-ttu-id="7e70a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e70a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e70a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e70a-132">-WhatIf</span></span>
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

### <span data-ttu-id="7e70a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e70a-133">CommonParameters</span></span>
<span data-ttu-id="7e70a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e70a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e70a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e70a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e70a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e70a-136">INPUTS</span></span>

### <span data-ttu-id="7e70a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7e70a-137">System.String</span></span>

### <span data-ttu-id="7e70a-138">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="7e70a-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="7e70a-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e70a-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e70a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e70a-140">OUTPUTS</span></span>

### <span data-ttu-id="7e70a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e70a-141">System.Boolean</span></span>

## <span data-ttu-id="7e70a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e70a-142">NOTES</span></span>

## <span data-ttu-id="7e70a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e70a-143">RELATED LINKS</span></span>
