---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520013"
---
# <span data-ttu-id="8dc8d-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8dc8d-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="8dc8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc8d-103">Удаляет пул файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="8dc8d-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="8dc8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dc8d-104">SYNTAX</span></span>

### <span data-ttu-id="8dc8d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dc8d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc8d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc8d-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc8d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc8d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc8d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc8d-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc8d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc8d-109">DESCRIPTION</span></span>
<span data-ttu-id="8dc8d-110">Для **удаления пула ANF будет удален cmdlet Remove-AzNetAppFilesPool.**</span><span class="sxs-lookup"><span data-stu-id="8dc8d-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="8dc8d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc8d-111">EXAMPLES</span></span>

### <span data-ttu-id="8dc8d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dc8d-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="8dc8d-113">Эта команда удаляет пул ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="8dc8d-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="8dc8d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc8d-114">PARAMETERS</span></span>

### <span data-ttu-id="8dc8d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8dc8d-115">-AccountName</span></span>
<span data-ttu-id="8dc8d-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="8dc8d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8dc8d-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="8dc8d-117">-AccountObject</span></span>
<span data-ttu-id="8dc8d-118">Объект учетной записи, содержащий пул для удаления</span><span class="sxs-lookup"><span data-stu-id="8dc8d-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc8d-119">-DefaultProfile</span></span>
<span data-ttu-id="8dc8d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc8d-121">-InputObject</span></span>
<span data-ttu-id="8dc8d-122">Объект пула, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="8dc8d-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc8d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc8d-123">-Name</span></span>
<span data-ttu-id="8dc8d-124">Имя пула ANF</span><span class="sxs-lookup"><span data-stu-id="8dc8d-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc8d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dc8d-125">-PassThru</span></span>
<span data-ttu-id="8dc8d-126">Возврат, был ли указанный пул успешно удален</span><span class="sxs-lookup"><span data-stu-id="8dc8d-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="8dc8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8dc8d-128">Группа ресурсов пула ANF</span><span class="sxs-lookup"><span data-stu-id="8dc8d-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="8dc8d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc8d-129">-ResourceId</span></span>
<span data-ttu-id="8dc8d-130">ИД ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="8dc8d-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="8dc8d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc8d-131">-Confirm</span></span>
<span data-ttu-id="8dc8d-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc8d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc8d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc8d-133">-WhatIf</span></span>
<span data-ttu-id="8dc8d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc8d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc8d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8dc8d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc8d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc8d-136">CommonParameters</span></span>
<span data-ttu-id="8dc8d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc8d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc8d-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dc8d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc8d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc8d-139">INPUTS</span></span>

### <span data-ttu-id="8dc8d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc8d-140">System.String</span></span>

### <span data-ttu-id="8dc8d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8dc8d-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="8dc8d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="8dc8d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="8dc8d-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc8d-143">OUTPUTS</span></span>

### <span data-ttu-id="8dc8d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8dc8d-144">System.Boolean</span></span>

## <span data-ttu-id="8dc8d-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dc8d-145">NOTES</span></span>

## <span data-ttu-id="8dc8d-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc8d-146">RELATED LINKS</span></span>
