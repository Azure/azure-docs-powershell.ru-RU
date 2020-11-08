---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074716"
---
# <span data-ttu-id="f68e7-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f68e7-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f68e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f68e7-102">SYNOPSIS</span></span>

<span data-ttu-id="f68e7-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f68e7-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="f68e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f68e7-104">SYNTAX</span></span>

### <span data-ttu-id="f68e7-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68e7-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f68e7-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f68e7-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f68e7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f68e7-107">DESCRIPTION</span></span>

<span data-ttu-id="f68e7-108">Командлет **Get-AzRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f68e7-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="f68e7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f68e7-109">EXAMPLES</span></span>

### <span data-ttu-id="f68e7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f68e7-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="f68e7-111">Получение списка хранилищ в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="f68e7-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="f68e7-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f68e7-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="f68e7-113">Получение списка хранилищ в группе ресурсов в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="f68e7-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="f68e7-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f68e7-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="f68e7-115">Получение хранилища в группе ресурсов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="f68e7-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="f68e7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f68e7-116">PARAMETERS</span></span>

### <span data-ttu-id="f68e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68e7-117">-DefaultProfile</span></span>

<span data-ttu-id="f68e7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f68e7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f68e7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f68e7-119">-Name</span></span>

<span data-ttu-id="f68e7-120">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="f68e7-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68e7-121">-ResourceGroupName</span></span>

<span data-ttu-id="f68e7-122">Указывает имя группы ресурсов Azure, из которой извлекается указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f68e7-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68e7-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="f68e7-123">-Tag</span></span>

<span data-ttu-id="f68e7-124">Указывает теги для запроса</span><span class="sxs-lookup"><span data-stu-id="f68e7-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68e7-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="f68e7-125">-TagName</span></span>

<span data-ttu-id="f68e7-126">Задает ключ тега для запроса</span><span class="sxs-lookup"><span data-stu-id="f68e7-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68e7-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="f68e7-127">-TagValue</span></span>

<span data-ttu-id="f68e7-128">Указывает значение тега для запроса</span><span class="sxs-lookup"><span data-stu-id="f68e7-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f68e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68e7-129">CommonParameters</span></span>
<span data-ttu-id="f68e7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f68e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68e7-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f68e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68e7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f68e7-132">INPUTS</span></span>

### <span data-ttu-id="f68e7-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="f68e7-133">None</span></span>

## <span data-ttu-id="f68e7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f68e7-134">OUTPUTS</span></span>

### <span data-ttu-id="f68e7-135">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="f68e7-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f68e7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="f68e7-136">NOTES</span></span>

## <span data-ttu-id="f68e7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f68e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="f68e7-138">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f68e7-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f68e7-139">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f68e7-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="f68e7-140">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f68e7-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
