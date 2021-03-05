---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968147"
---
# <span data-ttu-id="051ad-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="051ad-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="051ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="051ad-102">SYNOPSIS</span></span>
<span data-ttu-id="051ad-103">Обновляет учетную запись Azure NetApp Files (ANF) в соответствии с предоставленными необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="051ad-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="051ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="051ad-104">SYNTAX</span></span>

### <span data-ttu-id="051ad-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="051ad-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="051ad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="051ad-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="051ad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="051ad-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="051ad-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="051ad-108">DESCRIPTION</span></span>
<span data-ttu-id="051ad-109">При этом учетная запись ANF изменяется с учетной записью **Update-AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="051ad-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="051ad-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="051ad-110">EXAMPLES</span></span>

### <span data-ttu-id="051ad-111">Пример 1. Обновление учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="051ad-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="051ad-112">Эта команда выполняет обновление для учетной записи, изменяя теги на предоставленные.</span><span class="sxs-lookup"><span data-stu-id="051ad-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="051ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="051ad-113">PARAMETERS</span></span>

### <span data-ttu-id="051ad-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="051ad-114">-ActiveDirectory</span></span>
<span data-ttu-id="051ad-115">A hashtable array which represents the active directories</span><span class="sxs-lookup"><span data-stu-id="051ad-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051ad-116">-DefaultProfile</span></span>
<span data-ttu-id="051ad-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="051ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="051ad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="051ad-118">-InputObject</span></span>
<span data-ttu-id="051ad-119">Объект учетной записи, который нужно обновить</span><span class="sxs-lookup"><span data-stu-id="051ad-119">The account object to update</span></span>

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

### <span data-ttu-id="051ad-120">-Location</span><span class="sxs-lookup"><span data-stu-id="051ad-120">-Location</span></span>
<span data-ttu-id="051ad-121">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="051ad-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ad-122">-Name</span><span class="sxs-lookup"><span data-stu-id="051ad-122">-Name</span></span>
<span data-ttu-id="051ad-123">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="051ad-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="051ad-125">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="051ad-125">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ad-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="051ad-126">-ResourceId</span></span>
<span data-ttu-id="051ad-127">ИД ресурса учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="051ad-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="051ad-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="051ad-128">-Tag</span></span>
<span data-ttu-id="051ad-129">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="051ad-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051ad-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="051ad-130">-Confirm</span></span>
<span data-ttu-id="051ad-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="051ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="051ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="051ad-132">-WhatIf</span></span>
<span data-ttu-id="051ad-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="051ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="051ad-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="051ad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="051ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051ad-135">CommonParameters</span></span>
<span data-ttu-id="051ad-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="051ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051ad-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="051ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051ad-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="051ad-138">INPUTS</span></span>

### <span data-ttu-id="051ad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="051ad-139">System.String</span></span>

### <span data-ttu-id="051ad-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="051ad-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="051ad-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="051ad-141">OUTPUTS</span></span>

### <span data-ttu-id="051ad-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="051ad-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="051ad-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="051ad-143">NOTES</span></span>

## <span data-ttu-id="051ad-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="051ad-144">RELATED LINKS</span></span>
