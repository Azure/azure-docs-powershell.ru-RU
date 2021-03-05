---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: c5b8059561b859bd4ea7698b2cb41c9eb9a50a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968216"
---
# <span data-ttu-id="d90cf-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d90cf-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d90cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d90cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d90cf-103">Обновляет учетную запись Azure NetApp Files (ANF) с помощью нового набора данных.</span><span class="sxs-lookup"><span data-stu-id="d90cf-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="d90cf-104">Полезно для удаления связанных активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="d90cf-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="d90cf-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d90cf-105">SYNTAX</span></span>

### <span data-ttu-id="d90cf-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d90cf-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d90cf-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d90cf-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d90cf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d90cf-108">DESCRIPTION</span></span>
<span data-ttu-id="d90cf-109">**Cmdlet Set-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="d90cf-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d90cf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d90cf-110">EXAMPLES</span></span>

### <span data-ttu-id="d90cf-111">Пример 1. Изменение учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="d90cf-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="d90cf-112">Эта команда выполняет обновление для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d90cf-112">This command performs an update on the given account.</span></span> <span data-ttu-id="d90cf-113">Отсутствие активного каталога означает, что он будет удален из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d90cf-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="d90cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d90cf-114">PARAMETERS</span></span>

### <span data-ttu-id="d90cf-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d90cf-115">-ActiveDirectory</span></span>
<span data-ttu-id="d90cf-116">A hashtable array which represents the active directories</span><span class="sxs-lookup"><span data-stu-id="d90cf-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d90cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90cf-117">-DefaultProfile</span></span>
<span data-ttu-id="d90cf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d90cf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d90cf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d90cf-119">-Location</span></span>
<span data-ttu-id="d90cf-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="d90cf-120">The location of the resource</span></span>

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

### <span data-ttu-id="d90cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d90cf-121">-Name</span></span>
<span data-ttu-id="d90cf-122">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="d90cf-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="d90cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="d90cf-124">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="d90cf-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d90cf-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d90cf-125">-Tag</span></span>
<span data-ttu-id="d90cf-126">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="d90cf-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d90cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d90cf-127">-Confirm</span></span>
<span data-ttu-id="d90cf-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d90cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d90cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d90cf-129">-WhatIf</span></span>
<span data-ttu-id="d90cf-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d90cf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d90cf-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d90cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d90cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90cf-132">CommonParameters</span></span>
<span data-ttu-id="d90cf-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90cf-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d90cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90cf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d90cf-135">INPUTS</span></span>

### <span data-ttu-id="d90cf-136">Нет</span><span class="sxs-lookup"><span data-stu-id="d90cf-136">None</span></span>

## <span data-ttu-id="d90cf-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d90cf-137">OUTPUTS</span></span>

### <span data-ttu-id="d90cf-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d90cf-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d90cf-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d90cf-139">NOTES</span></span>

## <span data-ttu-id="d90cf-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d90cf-140">RELATED LINKS</span></span>
