---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 9fbc00fe190e0a53fc9c41a6894ec35a7f8d9129
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504624"
---
# <span data-ttu-id="b4849-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="b4849-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="b4849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4849-102">SYNOPSIS</span></span>
<span data-ttu-id="b4849-103">Удаляет учетные данные Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4849-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="b4849-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4849-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4849-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4849-105">DESCRIPTION</span></span>
<span data-ttu-id="b4849-106">Этот Remove-AzDataLakeAnalyticsCatalogCredential удаляет учетные данные каталога Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4849-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="b4849-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4849-107">EXAMPLES</span></span>

### <span data-ttu-id="b4849-108">Пример 1. Удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="b4849-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="b4849-109">Эта команда удаляет указанные учетные данные каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4849-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="b4849-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4849-110">PARAMETERS</span></span>

### <span data-ttu-id="b4849-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b4849-111">-Account</span></span>
<span data-ttu-id="b4849-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4849-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b4849-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4849-113">-DatabaseName</span></span>
<span data-ttu-id="b4849-114">Имя базы данных, в которой хранится учетная данные.</span><span class="sxs-lookup"><span data-stu-id="b4849-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="b4849-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4849-115">-DefaultProfile</span></span>
<span data-ttu-id="b4849-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4849-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4849-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4849-117">-Force</span></span>
<span data-ttu-id="b4849-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b4849-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4849-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b4849-119">-Name</span></span>
<span data-ttu-id="b4849-120">Указывает имя учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b4849-120">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="b4849-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4849-121">-PassThru</span></span>
<span data-ttu-id="b4849-122">Указывает на то, что этот cmdlet не ждет завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b4849-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="b4849-123">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b4849-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4849-124">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b4849-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4849-125">-Password</span><span class="sxs-lookup"><span data-stu-id="b4849-125">-Password</span></span>
<span data-ttu-id="b4849-126">Пароль учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b4849-126">The password for the credential.</span></span>
<span data-ttu-id="b4849-127">Это необходимо, если звоните не владельцем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b4849-127">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="b4849-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b4849-128">-Recurse</span></span>
<span data-ttu-id="b4849-129">Указывает на то, что при удалении необходимо удалить все ресурсы, зависящие от этих учетных данных, и удалить их.</span><span class="sxs-lookup"><span data-stu-id="b4849-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="b4849-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4849-130">-Confirm</span></span>
<span data-ttu-id="b4849-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4849-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4849-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4849-132">-WhatIf</span></span>
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

### <span data-ttu-id="b4849-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4849-133">CommonParameters</span></span>
<span data-ttu-id="b4849-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4849-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4849-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4849-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4849-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4849-136">INPUTS</span></span>

### <span data-ttu-id="b4849-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b4849-137">System.String</span></span>

### <span data-ttu-id="b4849-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="b4849-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="b4849-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b4849-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4849-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4849-140">OUTPUTS</span></span>

### <span data-ttu-id="b4849-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4849-141">System.Boolean</span></span>

## <span data-ttu-id="b4849-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4849-142">NOTES</span></span>

## <span data-ttu-id="b4849-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4849-143">RELATED LINKS</span></span>
