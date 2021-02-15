---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221361"
---
# <span data-ttu-id="fc744-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="fc744-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="fc744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc744-102">SYNOPSIS</span></span>
<span data-ttu-id="fc744-103">Сведения о конфигурации Azure NetApp Files (ANF) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fc744-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="fc744-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc744-104">SYNTAX</span></span>

### <span data-ttu-id="fc744-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc744-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc744-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc744-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc744-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc744-107">DESCRIPTION</span></span>
<span data-ttu-id="fc744-108">Для получения подробных сведений о конфигурации учетных записей ANF Active Directory можно получить сведения о **cmdlet Get-AzNetAppFilesActiveDirectory.**</span><span class="sxs-lookup"><span data-stu-id="fc744-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="fc744-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc744-109">EXAMPLES</span></span>

### <span data-ttu-id="fc744-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc744-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="fc744-111">Эта команда получает конфигурацию AD MyADConfigName для учетной записи Azure NetApp Files (ANF) с именем MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="fc744-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="fc744-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc744-112">PARAMETERS</span></span>

### <span data-ttu-id="fc744-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc744-113">-AccountName</span></span>
<span data-ttu-id="fc744-114">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="fc744-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="fc744-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="fc744-115">-AccountObject</span></span>
<span data-ttu-id="fc744-116">Учетная запись для нового объекта Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc744-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="fc744-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="fc744-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="fc744-118">The ActiveDirectoryId of the ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc744-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc744-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc744-119">-DefaultProfile</span></span>
<span data-ttu-id="fc744-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc744-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc744-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc744-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc744-122">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="fc744-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="fc744-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc744-123">CommonParameters</span></span>
<span data-ttu-id="fc744-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc744-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc744-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc744-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc744-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc744-126">INPUTS</span></span>

### <span data-ttu-id="fc744-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="fc744-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="fc744-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc744-128">OUTPUTS</span></span>

### <span data-ttu-id="fc744-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="fc744-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="fc744-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc744-130">NOTES</span></span>

## <span data-ttu-id="fc744-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc744-131">RELATED LINKS</span></span>
