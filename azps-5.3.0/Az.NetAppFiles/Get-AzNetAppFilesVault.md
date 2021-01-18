---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505021"
---
# <span data-ttu-id="52171-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="52171-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="52171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52171-102">SYNOPSIS</span></span>
<span data-ttu-id="52171-103">Получает список резервных копий учетных записей Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="52171-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="52171-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52171-104">SYNTAX</span></span>

### <span data-ttu-id="52171-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52171-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52171-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52171-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52171-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52171-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52171-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52171-108">DESCRIPTION</span></span>
<span data-ttu-id="52171-109">Для получения списка резервных копий учетных записей ANF возвращается список **cmdlet Get-AzNetAppFilesVault.**</span><span class="sxs-lookup"><span data-stu-id="52171-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="52171-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52171-110">EXAMPLES</span></span>

### <span data-ttu-id="52171-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52171-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="52171-112">Эта команда получает список резервных копий для учетной записи Azure NetappFiles (ANF) "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="52171-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="52171-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52171-113">PARAMETERS</span></span>

### <span data-ttu-id="52171-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52171-114">-AccountName</span></span>
<span data-ttu-id="52171-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="52171-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52171-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="52171-116">-AccountObject</span></span>
<span data-ttu-id="52171-117">Учетная запись для нового объекта резервной копии</span><span class="sxs-lookup"><span data-stu-id="52171-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="52171-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52171-118">-DefaultProfile</span></span>
<span data-ttu-id="52171-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52171-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52171-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52171-120">-ResourceGroupName</span></span>
<span data-ttu-id="52171-121">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="52171-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="52171-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52171-122">-ResourceId</span></span>
<span data-ttu-id="52171-123">ИД ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="52171-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="52171-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52171-124">CommonParameters</span></span>
<span data-ttu-id="52171-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52171-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52171-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52171-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52171-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52171-127">INPUTS</span></span>

### <span data-ttu-id="52171-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="52171-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="52171-129">System.String</span><span class="sxs-lookup"><span data-stu-id="52171-129">System.String</span></span>

## <span data-ttu-id="52171-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52171-130">OUTPUTS</span></span>

### <span data-ttu-id="52171-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="52171-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="52171-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52171-132">NOTES</span></span>

## <span data-ttu-id="52171-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52171-133">RELATED LINKS</span></span>
