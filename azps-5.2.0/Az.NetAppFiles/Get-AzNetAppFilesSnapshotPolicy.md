---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410799"
---
# <span data-ttu-id="aa927-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="aa927-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="aa927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa927-102">SYNOPSIS</span></span>
<span data-ttu-id="aa927-103">Сведения о политике моментального снимка в Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="aa927-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="aa927-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa927-104">SYNTAX</span></span>

### <span data-ttu-id="aa927-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa927-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa927-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa927-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa927-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa927-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa927-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa927-108">DESCRIPTION</span></span>
<span data-ttu-id="aa927-109">Чтобы получить сведения о политике моментального снимка ANF, можно получить подробные сведения о политике **Get-AzNetAppFilesSnapshotPolicy.**</span><span class="sxs-lookup"><span data-stu-id="aa927-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="aa927-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa927-110">EXAMPLES</span></span>

### <span data-ttu-id="aa927-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa927-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="aa927-112">Эта команда получает политику резервного копирования MyBackupPolicy для учетной записи MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="aa927-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="aa927-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa927-113">PARAMETERS</span></span>

### <span data-ttu-id="aa927-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa927-114">-AccountName</span></span>
<span data-ttu-id="aa927-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="aa927-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="aa927-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="aa927-116">-AccountObject</span></span>
<span data-ttu-id="aa927-117">Учетная запись для нового объекта политики моментального снимка</span><span class="sxs-lookup"><span data-stu-id="aa927-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="aa927-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa927-118">-DefaultProfile</span></span>
<span data-ttu-id="aa927-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa927-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa927-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aa927-120">-Name</span></span>
<span data-ttu-id="aa927-121">Имя политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="aa927-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa927-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa927-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa927-123">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="aa927-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="aa927-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa927-124">-ResourceId</span></span>
<span data-ttu-id="aa927-125">ИД ресурса политики моментального снимка ANF</span><span class="sxs-lookup"><span data-stu-id="aa927-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="aa927-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa927-126">-Confirm</span></span>
<span data-ttu-id="aa927-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa927-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa927-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa927-128">-WhatIf</span></span>
<span data-ttu-id="aa927-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa927-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa927-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa927-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa927-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa927-131">CommonParameters</span></span>
<span data-ttu-id="aa927-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa927-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa927-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa927-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa927-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa927-134">INPUTS</span></span>

### <span data-ttu-id="aa927-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aa927-135">System.String</span></span>

### <span data-ttu-id="aa927-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="aa927-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="aa927-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa927-137">OUTPUTS</span></span>

### <span data-ttu-id="aa927-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="aa927-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="aa927-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa927-139">NOTES</span></span>

## <span data-ttu-id="aa927-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa927-140">RELATED LINKS</span></span>
