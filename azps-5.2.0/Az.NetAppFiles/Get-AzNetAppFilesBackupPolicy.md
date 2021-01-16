---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410828"
---
# <span data-ttu-id="cddad-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="cddad-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="cddad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddad-102">SYNOPSIS</span></span>
<span data-ttu-id="cddad-103">Сведения о политике резервного копирования Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="cddad-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="cddad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cddad-104">SYNTAX</span></span>

### <span data-ttu-id="cddad-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cddad-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cddad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cddad-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cddad-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cddad-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cddad-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cddad-108">DESCRIPTION</span></span>
<span data-ttu-id="cddad-109">Для получения сведений о политике резервного копирования ANF возвращается сведения о cmdlet **Get-AzNetAppFilesBackupPolicy.**</span><span class="sxs-lookup"><span data-stu-id="cddad-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="cddad-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cddad-110">EXAMPLES</span></span>

### <span data-ttu-id="cddad-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cddad-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="cddad-112">Эта команда получает политику резервного копирования MyBackupPolicy для учетной записи MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="cddad-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="cddad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cddad-113">PARAMETERS</span></span>

### <span data-ttu-id="cddad-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cddad-114">-AccountName</span></span>
<span data-ttu-id="cddad-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="cddad-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="cddad-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="cddad-116">-AccountObject</span></span>
<span data-ttu-id="cddad-117">Объект Account, содержащий политику резервного копирования, возвращаемую</span><span class="sxs-lookup"><span data-stu-id="cddad-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="cddad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddad-118">-DefaultProfile</span></span>
<span data-ttu-id="cddad-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cddad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddad-120">-Name</span><span class="sxs-lookup"><span data-stu-id="cddad-120">-Name</span></span>
<span data-ttu-id="cddad-121">Имя политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="cddad-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddad-122">-ResourceGroupName</span></span>
<span data-ttu-id="cddad-123">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="cddad-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="cddad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddad-124">-ResourceId</span></span>
<span data-ttu-id="cddad-125">Код ресурса политики резервного копирования ANF</span><span class="sxs-lookup"><span data-stu-id="cddad-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="cddad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddad-126">CommonParameters</span></span>
<span data-ttu-id="cddad-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cddad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddad-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cddad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddad-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cddad-129">INPUTS</span></span>

### <span data-ttu-id="cddad-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cddad-130">System.String</span></span>

### <span data-ttu-id="cddad-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="cddad-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="cddad-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cddad-132">OUTPUTS</span></span>

### <span data-ttu-id="cddad-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="cddad-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="cddad-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cddad-134">NOTES</span></span>

## <span data-ttu-id="cddad-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cddad-135">RELATED LINKS</span></span>
