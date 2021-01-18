---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506010"
---
# <span data-ttu-id="b720a-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b720a-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b720a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b720a-102">SYNOPSIS</span></span>

<span data-ttu-id="b720a-103">Получает список сейфов служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b720a-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="b720a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b720a-104">SYNTAX</span></span>

### <span data-ttu-id="b720a-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b720a-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b720a-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b720a-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b720a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b720a-107">DESCRIPTION</span></span>

<span data-ttu-id="b720a-108">Для **получения списка сейфов служб** восстановления в текущей подписке возвращается список хранилищ Службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="b720a-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="b720a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b720a-109">EXAMPLES</span></span>

### <span data-ttu-id="b720a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b720a-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="b720a-111">Получить список сейфа в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="b720a-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="b720a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b720a-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="b720a-113">Получить список хранилища в группе ресурсов выбранной подписки.</span><span class="sxs-lookup"><span data-stu-id="b720a-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="b720a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b720a-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="b720a-115">Первый из них получает хранилище в группе ресурсов с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="b720a-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="b720a-116">Затем мы будем получать доступ к данным MSI из хранилища.</span><span class="sxs-lookup"><span data-stu-id="b720a-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="b720a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b720a-117">PARAMETERS</span></span>

### <span data-ttu-id="b720a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b720a-118">-DefaultProfile</span></span>

<span data-ttu-id="b720a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b720a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b720a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b720a-120">-Name</span></span>

<span data-ttu-id="b720a-121">Указывает имя хранилища, для которого нужно получить запрос.</span><span class="sxs-lookup"><span data-stu-id="b720a-121">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="b720a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b720a-122">-ResourceGroupName</span></span>

<span data-ttu-id="b720a-123">Имя группы ресурсов Azure, из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b720a-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="b720a-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b720a-124">-Tag</span></span>

<span data-ttu-id="b720a-125">Указывает теги для запроса</span><span class="sxs-lookup"><span data-stu-id="b720a-125">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="b720a-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="b720a-126">-TagName</span></span>

<span data-ttu-id="b720a-127">Ключ запроса "Тег" для</span><span class="sxs-lookup"><span data-stu-id="b720a-127">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="b720a-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="b720a-128">-TagValue</span></span>

<span data-ttu-id="b720a-129">Значение тега для запроса</span><span class="sxs-lookup"><span data-stu-id="b720a-129">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="b720a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b720a-130">CommonParameters</span></span>
<span data-ttu-id="b720a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b720a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b720a-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b720a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b720a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b720a-133">INPUTS</span></span>

### <span data-ttu-id="b720a-134">Нет</span><span class="sxs-lookup"><span data-stu-id="b720a-134">None</span></span>

## <span data-ttu-id="b720a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b720a-135">OUTPUTS</span></span>

### <span data-ttu-id="b720a-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="b720a-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b720a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b720a-137">NOTES</span></span>
<span data-ttu-id="b720a-138">Get-AzRecoveryServicesVault az.RecoveryServices(<=2.10.0) не может работать с Az.Accounts(>=1.8.1) из-за неправильной ссылки на сборку.</span><span class="sxs-lookup"><span data-stu-id="b720a-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="b720a-139">Если вы используете последние учетные записи Az или Az.Accounts, модуль Az.RecoveryServices необходимо обновить до версии 2.11.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b720a-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="b720a-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b720a-140">RELATED LINKS</span></span>

[<span data-ttu-id="b720a-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b720a-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b720a-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b720a-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="b720a-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b720a-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
