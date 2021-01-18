---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504575"
---
# <span data-ttu-id="74bc8-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="74bc8-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="74bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="74bc8-103">Удаляет учетную запись Data Lake Store навсегда.</span><span class="sxs-lookup"><span data-stu-id="74bc8-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="74bc8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74bc8-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74bc8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="74bc8-106">При **этом учетная** запись Компании Data Lake Store удаляется окончательно.</span><span class="sxs-lookup"><span data-stu-id="74bc8-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="74bc8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="74bc8-108">Пример 1. Удаление учетной записи Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="74bc8-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="74bc8-109">Эта команда удаляет учетную запись ContosoADL из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74bc8-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="74bc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74bc8-110">PARAMETERS</span></span>

### <span data-ttu-id="74bc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bc8-111">-DefaultProfile</span></span>
<span data-ttu-id="74bc8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="74bc8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74bc8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="74bc8-113">-Force</span></span>
<span data-ttu-id="74bc8-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="74bc8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74bc8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="74bc8-115">-Name</span></span>
<span data-ttu-id="74bc8-116">Указывает имя удаляемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="74bc8-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="74bc8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74bc8-117">-PassThru</span></span>
<span data-ttu-id="74bc8-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="74bc8-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74bc8-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="74bc8-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74bc8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74bc8-120">-ResourceGroupName</span></span>
<span data-ttu-id="74bc8-121">Определяет группу ресурсов, которая содержит удаляемую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="74bc8-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="74bc8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74bc8-122">-Confirm</span></span>
<span data-ttu-id="74bc8-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74bc8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74bc8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74bc8-124">-WhatIf</span></span>
<span data-ttu-id="74bc8-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74bc8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74bc8-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="74bc8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74bc8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bc8-127">CommonParameters</span></span>
<span data-ttu-id="74bc8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bc8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bc8-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74bc8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bc8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74bc8-130">INPUTS</span></span>

### <span data-ttu-id="74bc8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="74bc8-131">System.String</span></span>

## <span data-ttu-id="74bc8-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74bc8-132">OUTPUTS</span></span>

### <span data-ttu-id="74bc8-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74bc8-133">System.Boolean</span></span>

## <span data-ttu-id="74bc8-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74bc8-134">NOTES</span></span>

## <span data-ttu-id="74bc8-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74bc8-135">RELATED LINKS</span></span>

[<span data-ttu-id="74bc8-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="74bc8-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="74bc8-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="74bc8-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="74bc8-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="74bc8-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="74bc8-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="74bc8-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


