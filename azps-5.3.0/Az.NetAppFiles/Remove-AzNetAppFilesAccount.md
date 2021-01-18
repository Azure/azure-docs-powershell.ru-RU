---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518170"
---
# <span data-ttu-id="6e677-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6e677-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="6e677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e677-102">SYNOPSIS</span></span>
<span data-ttu-id="6e677-103">Удаляет учетную запись Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="6e677-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="6e677-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e677-104">SYNTAX</span></span>

### <span data-ttu-id="6e677-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e677-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e677-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e677-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e677-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e677-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e677-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e677-108">DESCRIPTION</span></span>
<span data-ttu-id="6e677-109">Для удаления учетной записи ANF будет удалена учетная запись **Remove-AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="6e677-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="6e677-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e677-110">EXAMPLES</span></span>

### <span data-ttu-id="6e677-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e677-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="6e677-112">Эта команда удаляет учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="6e677-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="6e677-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e677-113">PARAMETERS</span></span>

### <span data-ttu-id="6e677-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e677-114">-DefaultProfile</span></span>
<span data-ttu-id="6e677-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e677-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e677-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e677-116">-InputObject</span></span>
<span data-ttu-id="6e677-117">Удаляемый объект учетной записи</span><span class="sxs-lookup"><span data-stu-id="6e677-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e677-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6e677-118">-Name</span></span>
<span data-ttu-id="6e677-119">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6e677-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e677-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e677-120">-PassThru</span></span>
<span data-ttu-id="6e677-121">Возврат, была ли указанная учетная запись успешно удалена</span><span class="sxs-lookup"><span data-stu-id="6e677-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="6e677-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e677-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e677-123">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6e677-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e677-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e677-124">-ResourceId</span></span>
<span data-ttu-id="6e677-125">ИД ресурса учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="6e677-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e677-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e677-126">-Confirm</span></span>
<span data-ttu-id="6e677-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e677-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e677-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e677-128">-WhatIf</span></span>
<span data-ttu-id="6e677-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e677-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e677-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e677-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e677-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e677-131">CommonParameters</span></span>
<span data-ttu-id="6e677-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e677-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e677-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e677-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e677-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e677-134">INPUTS</span></span>

### <span data-ttu-id="6e677-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6e677-135">System.String</span></span>

### <span data-ttu-id="6e677-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="6e677-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6e677-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e677-137">OUTPUTS</span></span>

### <span data-ttu-id="6e677-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e677-138">System.Boolean</span></span>

## <span data-ttu-id="6e677-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e677-139">NOTES</span></span>

## <span data-ttu-id="6e677-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e677-140">RELATED LINKS</span></span>
