---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422487"
---
# <span data-ttu-id="86d49-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="86d49-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="86d49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d49-102">SYNOPSIS</span></span>
<span data-ttu-id="86d49-103">Обновляет учетную запись Azure NetApp Files (ANF) с учетом предоставленных необязательных модификаторов.</span><span class="sxs-lookup"><span data-stu-id="86d49-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="86d49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86d49-104">SYNTAX</span></span>

### <span data-ttu-id="86d49-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86d49-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d49-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d49-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86d49-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86d49-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d49-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86d49-108">DESCRIPTION</span></span>
<span data-ttu-id="86d49-109">Для **учетной записи ANF изменяется cmdlet Update-AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="86d49-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="86d49-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86d49-110">EXAMPLES</span></span>

### <span data-ttu-id="86d49-111">Пример 1. Обновление учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="86d49-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="86d49-112">Эта команда выполняет обновление для учетной записи, изменяя теги на предоставленные.</span><span class="sxs-lookup"><span data-stu-id="86d49-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="86d49-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86d49-113">PARAMETERS</span></span>

### <span data-ttu-id="86d49-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="86d49-114">-ActiveDirectory</span></span>
<span data-ttu-id="86d49-115">A hashtable array which represents the active directories</span><span class="sxs-lookup"><span data-stu-id="86d49-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="86d49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d49-116">-DefaultProfile</span></span>
<span data-ttu-id="86d49-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86d49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d49-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d49-118">-InputObject</span></span>
<span data-ttu-id="86d49-119">Объект учетной записи, который нужно обновить</span><span class="sxs-lookup"><span data-stu-id="86d49-119">The account object to update</span></span>

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

### <span data-ttu-id="86d49-120">-Location</span><span class="sxs-lookup"><span data-stu-id="86d49-120">-Location</span></span>
<span data-ttu-id="86d49-121">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="86d49-121">The location of the resource</span></span>

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

### <span data-ttu-id="86d49-122">-Name</span><span class="sxs-lookup"><span data-stu-id="86d49-122">-Name</span></span>
<span data-ttu-id="86d49-123">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="86d49-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="86d49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d49-124">-ResourceGroupName</span></span>
<span data-ttu-id="86d49-125">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="86d49-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="86d49-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86d49-126">-ResourceId</span></span>
<span data-ttu-id="86d49-127">ИД ресурса учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="86d49-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="86d49-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="86d49-128">-Tag</span></span>
<span data-ttu-id="86d49-129">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="86d49-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="86d49-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86d49-130">-Confirm</span></span>
<span data-ttu-id="86d49-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d49-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d49-132">-WhatIf</span></span>
<span data-ttu-id="86d49-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d49-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d49-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86d49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d49-135">CommonParameters</span></span>
<span data-ttu-id="86d49-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d49-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86d49-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d49-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86d49-138">INPUTS</span></span>

### <span data-ttu-id="86d49-139">System.String</span><span class="sxs-lookup"><span data-stu-id="86d49-139">System.String</span></span>

### <span data-ttu-id="86d49-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="86d49-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="86d49-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86d49-141">OUTPUTS</span></span>

### <span data-ttu-id="86d49-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="86d49-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="86d49-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86d49-143">NOTES</span></span>

## <span data-ttu-id="86d49-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86d49-144">RELATED LINKS</span></span>
