---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ab7607dd358e7c439539e99d44b263136f07cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968360"
---
# <span data-ttu-id="0cec3-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cec3-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cec3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cec3-103">Удаляет конфигурацию active directory Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="0cec3-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="0cec3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0cec3-104">SYNTAX</span></span>

### <span data-ttu-id="0cec3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0cec3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cec3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cec3-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cec3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cec3-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cec3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cec3-108">DESCRIPTION</span></span>
<span data-ttu-id="0cec3-109">Для удаления конфигурации Active Directory anF удаляется **cmdlet Remove-AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="0cec3-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="0cec3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0cec3-110">EXAMPLES</span></span>

### <span data-ttu-id="0cec3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0cec3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="0cec3-112">Эта команда удаляет новую конфигурацию active directory ANF с именем MyADName.</span><span class="sxs-lookup"><span data-stu-id="0cec3-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="0cec3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cec3-113">PARAMETERS</span></span>

### <span data-ttu-id="0cec3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cec3-114">-AccountName</span></span>
<span data-ttu-id="0cec3-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0cec3-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0cec3-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0cec3-116">-AccountObject</span></span>
<span data-ttu-id="0cec3-117">Учетная запись для объекта Active Directory</span><span class="sxs-lookup"><span data-stu-id="0cec3-117">The Account for the Active Directory object</span></span>

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

### <span data-ttu-id="0cec3-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="0cec3-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="0cec3-119">ИД активного каталога ANF</span><span class="sxs-lookup"><span data-stu-id="0cec3-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cec3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cec3-120">-DefaultProfile</span></span>
<span data-ttu-id="0cec3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0cec3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cec3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cec3-122">-InputObject</span></span>
<span data-ttu-id="0cec3-123">Удаляемый объект Active Directory</span><span class="sxs-lookup"><span data-stu-id="0cec3-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cec3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cec3-124">-PassThru</span></span>
<span data-ttu-id="0cec3-125">Возвращает, была ли указанная active Directory успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="0cec3-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="0cec3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cec3-126">-ResourceGroupName</span></span>
<span data-ttu-id="0cec3-127">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="0cec3-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="0cec3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cec3-128">-Confirm</span></span>
<span data-ttu-id="0cec3-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0cec3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cec3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cec3-130">-WhatIf</span></span>
<span data-ttu-id="0cec3-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cec3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cec3-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0cec3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cec3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cec3-133">CommonParameters</span></span>
<span data-ttu-id="0cec3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cec3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cec3-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cec3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cec3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cec3-136">INPUTS</span></span>

### <span data-ttu-id="0cec3-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0cec3-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="0cec3-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cec3-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cec3-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0cec3-139">OUTPUTS</span></span>

### <span data-ttu-id="0cec3-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="0cec3-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="0cec3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0cec3-141">NOTES</span></span>

## <span data-ttu-id="0cec3-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cec3-142">RELATED LINKS</span></span>
